<script lang="ts">
    import { createEventDispatcher } from "svelte";

    // Create a dispatcher for component events
    const dispatch = createEventDispatcher();

    // Define props
    export let flashCard = {
        id: 0,
        question: "",
        answer: "",
    };

    // State variables
    let userAnswer = "";
    let feedback = "";
    let showFeedback = false;
    let isCorrect = false;

    // Function to check the answer
    function checkAnswer() {
        // Compare user answer with the correct answer (case insensitive)
        isCorrect =
            userAnswer.trim().toLowerCase() === flashCard.answer.toLowerCase();
        feedback = isCorrect
            ? "Goed gedaan! 🎉"
            : `Jammer. 🙈 Het goede antwoord is: ${flashCard.answer}`;
        showFeedback = true;

        // Dispatch event to parent component
        dispatch("answerSubmitted", { isCorrect });
    }

    // Reset the input field and feedback when flashCard changes
    $: if (flashCard) {
        userAnswer = "";
        showFeedback = false;
        feedback = "";
    }
</script>

<div class="flash-card">
    <div class="card-inner">
        <div class="question">
            <h2>{flashCard.question}</h2>
        </div>

        <div class="answer-section">
            <input
                type="text"
                bind:value={userAnswer}
                placeholder="Type jouw antwoord hier…"
                on:keydown={(e) => e.key === "Enter" && checkAnswer()}
            />
            <button on:click={checkAnswer}>Submit</button>
        </div>

        {#if showFeedback}
            <div
                class="feedback"
                class:correct={isCorrect}
                class:incorrect={!isCorrect}
            >
                {feedback}
            </div>
        {/if}
    </div>
</div>

<style>
    .flash-card {
        width: 100%;
        perspective: 1000px;
    }

    .card-inner {
        background-color: white;
        border-radius: 10px;
        box-shadow: 0 6px 16px rgba(0, 76, 80, 0.15);
        padding: 25px;
        min-height: 220px;
        display: flex;
        flex-direction: column;
        transition: all 0.6s ease;
        transform-style: preserve-3d;
        border: 2px solid #10abb4;
    }

    .card-inner:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 24px rgba(0, 76, 80, 0.2);
    }

    .question {
        flex-grow: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 25px;
        padding: 15px;
        background-color: rgba(0, 147, 156, 0.05);
        border-radius: 8px;
    }

    h2 {
        text-align: center;
        color: #004c50;
        font-size: 1.6rem;
        font-weight: 600;
        line-height: 1.4;
    }

    .answer-section {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }

    input {
        padding: 12px 16px;
        font-size: 1.1rem;
        border: 2px solid #10abb4;
        border-radius: 6px;
        color: #004c50;
        background-color: rgba(16, 171, 180, 0.05);
        transition: all 0.3s ease;
    }

    input:focus {
        outline: none;
        border-color: #00939c;
        box-shadow: 0 0 0 3px rgba(0, 147, 156, 0.2);
    }

    input::placeholder {
        color: rgba(0, 76, 80, 0.5);
    }

    button {
        background-color: #00939c;
        color: white;
        border: none;
        padding: 12px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin-top: 12px;
        cursor: pointer;
        border-radius: 6px;
        transition: all 0.3s ease;
        font-weight: 600;
        box-shadow: 0 2px 4px rgba(0, 76, 80, 0.2);
    }

    button:hover {
        background-color: #10abb4;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 76, 80, 0.3);
    }

    button:active {
        transform: translateY(0);
        box-shadow: 0 1px 2px rgba(0, 76, 80, 0.2);
    }

    .feedback {
        margin-top: 20px;
        padding: 15px;
        border-radius: 6px;
        text-align: center;
        font-size: 1.1rem;
        font-weight: 500;
        background-color: #9c3e00;
        box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
        animation: fadeIn 0.5s ease-out;
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: translateY(10px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .correct {
        background-color: rgba(16, 171, 180, 0.2);
        color: #004c50;
        border-left: 4px solid #10abb4;
    }

    .incorrect {
        background-color: rgba(156, 62, 0, 0.1);
        color: #502000;
        border-left: 4px solid #9c3e00;
    }
</style>
