<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        // 3A
        //{ id: 1, question: "Troianus", answer: "Trojaan" },
        //{ id: 2, question: "est", answer: "is" },
        //{ id: 3, question: "currere", answer: "rennen" },
        //{ id: 4, question: "fugerre", answer: "vluchten" },
        //{ id: 5, question: "non", answer: "niet" },
        //{ id: 6, question: "senex", answer: "oude man" },
        //{ id: 7, question: "enim", answer: "immers" },
        //{ id: 8, question: "puer", answer: "jongen" },
        //{ id: 9, question: "et", answer: "en" },
        //{ id: 10, question: "cur", answer: "waarom" },
        //{ id: 11, question: "timére", answer: "bang zijn" },
        //{ id: 12, question: "bellum", answer: "oorlog" },
        //{ id: 13, question: "saevire", answer: "woeden" },
        //// 3B
        //{ id: 14, question: "quoque", answer: "ook" },
        //{ id: 15, question: "sed", answer: "maar" },
        //{ id: 16, question: "eheu", answer: "ach" },
        //{ id: 17, question: "cadere", answer: "vallen" },
        //{ id: 18, question: "clamare", answer: "roepen" },
        //{ id: 19, question: "at", answer: "maar" },
        //{ id: 20, question: "neque…neque", answer: "noch...noch" },
        //{ id: 21, question: "audire", answer: "horen" },
        //{ id: 22, question: "omnes", answer: "alle" },
        //{ id: 23, question: "consistere", answer: "blijven staan" },
        //{ id: 24, question: "rogare", answer: "vragen" },
        //{ id: 25, question: "ubi", answer: "waar" },
        //{ id: 26, question: "femina", answer: "vrouw" },
        //{ id: 27, question: "autem", answer: "echter" },
        //{ id: 28, question: "respondére", answer: "antwoorden" },
        //{ id: 29, question: "iterum", answer: "weer" },
        //{ id: 30, question: "tum-", answer: "dan" },
        //{ id: 31, question: "tacére", answer: "zwijgen" },
        //{ id: 32, question: "pergere", answer: "gaan" },
        //{ id: 33, question: "Graecus", answer: "Griek" },
        //{ id: 34, question: "appropinquare", answer: "naderen" },
        //{ id: 35, question: "repetere", answer: "teruggaan" },
        //// 3C
        //{ id: 36, question: "errare", answer: "ronddwalen" },
        //{ id: 37, question: "quaerere", answer: "zoeken" },
        //{ id: 38, question: "fuga", answer: "vlucht" },
        //{ id: 39, question: "subito", answer: "plotseling" },
        //{ id: 40, question: "umbra", answer: "schim" },
        //{ id: 41, question: "apparére", answer: "verschijnen" },
        //{ id: 42, question: "dicere", answer: "zeggen" },
        //{ id: 43, question: "patria", answer: "vaderland" },
        //{ id: 44, question: "novus", answer: "nieuw" },
        //{ id: 45, question: "regnum", answer: "koninkrijk" },
        //{ id: 46, question: "manére", answer: "wachten" },
        //{ id: 47, question: "demum", answer: "pas" },
        //{ id: 48, question: "parére", answer: "gehoorzamen" },
        ////3D
        //{ id: 49, question: "navis, naves", answer: "schip" },
        //{ id: 50, question: "mare, maria", answer: "zee" },
        //{ id: 51, question: "stare", answer: "staan" },
        //{ id: 52, question: "lacrimare", answer: "huilen" },
        //{ id: 53, question: "procul", answer: "ver weg" },
        //{ id: 65, question: "etiam", answer: "ook" },
        //{ id: 66, question: "dormire", answer: "slapen" },
        //{ id: 67, question: "ludere", answer: "spelen" },
        //{ id: 68, question: "et", answer: "en" },
        //{ id: 69, question: "sunt", answer: "zijn" },
        //{ id: 70, question: "dolére", answer: "verdrietig zijn" },
        //{ id: 71, question: "nam", answer: "want" },
        //{ id: 72, question: "quo", answer: "waarheen" },
        //{ id: 73, question: "nescire", answer: "niet weten" },
        //{ id: 74, question: "servus", answer: "slaaf" },
        //{ id: 75, question: "serva", answer: "slavin" },
        // 6A
        //{ id: 76, question: "dolus", answer: "list" },
        //{ id: 77, question: "parare", answer: "voorbereiden" },
        //{ id: 78, question: "filius", answer: "zoon" },
        //{ id: 79, question: "natus", answer: "zoon" },
        //{ id: 80, question: "adiuvare", answer: "helpen" },
        //{ id: 81, question: "fallere", answer: "bedriegen" },
        //{ id: 82, question: "Carthago", answer: "Carthago" },
        //{ id: 83, question: "donum", answer: "geschenk" },
        //{ id: 84, question: "ire", answer: "gaan" },
        //{ id: 85, question: "ferre", answer: "brengen" },
        //{ id: 86, question: "nunc", answer: "nu" },
        //{ id: 87, question: "mandare", answer: "opdragen" },
        //{ id: 88, question: "forma", answer: "vorm" },
        //{ id: 89, question: "petere", answer: "gaan" },
        //{ id: 90, question: "amor, amores", answer: "liefde" },
        //{ id: 91, question: "cor, corda", answer: "hart" },
        //{ id: 92, question: "excitare", answer: "opwekken" },
        //{ id: 93, question: "parére", answer: "gehoorzamen" },
        //{ id: 94, question: "deponere", answer: "neerzetten" },
        //{ id: 95, question: "appropinquare", answer: "naderen" },
        //{ id: 96, question: "regia", answer: "paleis" },
        //{ id: 97, question: "lectus", answer: "bed" },
        //{ id: 98, question: "tollere", answer: "opheffen" },
        //{ id: 99, question: "mons, montes", answer: "berg" },
        //{ id: 100, question: "inter", answer: "tussen" },
        //{ id: 101, question: "flos, flores", answer: "bloem" },
        ////6B
        //{ id: 102, question: "intrare", answer: "binnengaan" },
        //{ id: 103, question: "sedes", answer: "zetel" },
        //{ id: 104, question: "Tyrius", answer: "Tyrier" },
        //{ id: 105, question: "convenire", answer: "samenkomen" },
        //{ id: 106, question: "vestis", answer: "kleding" },
        //{ id: 107, question: "tegere", answer: "bedekken" },
        //{ id: 108, question: "ubique", answer: "overal" },
        //{ id: 109, question: "-que", answer: "en" },
        //{ id: 110, question: "cena", answer: "maaltijd" },
        //{ id: 111, question: "centum", answer: "100" },
        //{ id: 112, question: "hospes", answer: "gast" },
        //{ id: 113, question: "excipere", answer: "ontvangen" },
        //{ id: 114, question: "alii…alii", answer: "sommigen anderen" },
        //{ id: 115, question: "mensa", answer: "tafel" },
        //{ id: 116, question: "vinum", answer: "wijn" },
        //{ id: 117, question: "implére", answer: "vullen" },
        //{ id: 118, question: "distribuere", answer: "uitdelen" },
        //{ id: 119, question: "adire", answer: "gaan naar" },
        //{ id: 120, question: "dare", answer: "geven" },
        //{ id: 121, question: "et…et", answer: "zowel als" },
        //{ id: 122, question: "movére", answer: "bewegen" },
        //{ id: 123, question: "accipere", answer: "ontvangen" },
        //{ id: 124, question: "memoria", answer: "herinnering" },
        //{ id: 125, question: "animus", answer: "hart" },
        //{ id: 126, question: "paulatim", answer: "langzamerhand" },
        //{ id: 127, question: "expellere", answer: "verdrijven" },
        // 7A
        //{ id: 128, question: "annus", answer: "jaar" },
        //{ id: 129, question: "decimus", answer: "tiende" },
        //{ id: 130, question: "nondum", answer: "nog niet" },
        //{ id: 131, question: "capere", answer: "nemen" },
        //{ id: 131, question: "itaque", answer: "dus" },
        //{ id: 132, question: "primo", answer: "eerst" },
        //{ id: 133, question: "auxilium", answer: "hulp" },
        //{ id: 134, question: "equus", answer: "paard" },
        //{ id: 135, question: "clam", answer: "in het geheim" },
        //{ id: 136, question: "aedificere", answer: "bouwen" },
        //{ id: 137, question: "complere", answer: "vullen" },
        //{ id: 138, question: "ceteri", answer: "overige" },
        //{ id: 139, question: "nocte", answer: "s nachts" },
        //{ id: 140, question: "a / ab", answer: "vanaf" },
        //{ id: 141, question: "ora", answer: "kust" },
        //{ id: 142, question: "navigare", answer: "varen" },
        //{ id: 143, question: "occultare", answer: "verbergen" },
        //{ id: 144, question: "insula", answer: "eiland" },
        //{ id: 145, question: "in", answer: "in" },
        //{ id: 146, question: "relinquere", answer: "verlaten" },
        //{ id: 147, question: "de", answer: "vanaf" },
        //{ id: 148, question: "murus", answer: "muur" },
        //{ id: 149, question: "spectare", answer: "kijken" },
        //{ id: 150, question: "nec…nec", answer: "noch noch" },
        //{ id: 151, question: "castra", answer: "legerkamp" },
        //{ id: 152, question: "laetus", answer: "verheugd" },
        //{ id: 153, question: "porta", answer: "poort" },
        //{ id: 154, question: "aperire", answer: "openen" },
        //{ id: 155, question: "an", answer: "of" },
        //{ id: 156, question: "flamma", answer: "vlam" },
        //{ id: 157, question: "urere", answer: "verbranden" },
        //{ id: 158, question: "intra", answer: "binnen" },
        //{ id: 159, question: "ducere", answer: "leiden" },
        //// 7B                 
        //{ id: 160, question: "sacerdos", answer: "priester" },
        //{ id: 161, question: "cum", answer: "met" },
        //{ id: 162, question: "e / ex", answer: "uit" },
        //{ id: 163, question: "credere", answer: "geloven" },
        //{ id: 164, question: "numquam", answer: "nooit" },
        //{ id: 165, question: "carére", answer: "missen" },
        //{ id: 166, question: "milites", answer: "soldaat" },
        //{ id: 167, question: "certe", answer: "zeker" },
        //{ id: 168, question: "timére", answer: "vrezen" },
        //{ id: 169, question: "hasta", answer: "lans" },
        //{ id: 170, question: "haerére", answer: "blijven steken" },
        //{ id: 171, question: "ecce", answer: "kijk" },
        //{ id: 172, question: "rex, reges", answer: "koning" },
        //{ id: 173, question: "trahere", answer: "trekken" },
        //{ id: 174, question: "nomen, nomina", answer: "naam" },
        //{ id: 175, question: "sine", answer: "zonder" },
        ////7C 
        //{ id: 176, question: "per", answer: "over" },
        //{ id: 177, question: "sanguis", answer: "bloed" },
        //{ id: 178, question: "lingua", answer: "tong" },
        //{ id: 179, question: "petere", answer: "gaan naar" },
        //{ id: 180, question: "primum", answer: "eerst" },
        //{ id: 181, question: "invadere", answer: "binnenvallen" },
        //{ id: 182, question: "corpus", answer: "lichaam" },
        //{ id: 183, question: "dens", answer: "tand" },
        //{ id: 184, question: "venenum", answer: "vergif" },
        //{ id: 185, question: "necare", answer: "doden" },
        //{ id: 186, question: "temptare", answer: "proberen" },
        //{ id: 187, question: "clamor", answer: "geschreeuw" },
        //{ id: 188, question: "frustra", answer: "tevergeefs" },
        //{ id: 189, question: "mors", answer: "dood" },
        //{ id: 190, question: "horrere", answer: "huiveren" },
        //{ id: 191, question: "modus", answer: "manier" },
        //{ id: 192, question: "punire", answer: "straffen" },
        ////8A
        //{ id: 193, question: "arma", answer: "wapens" },
        //{ id: 194, question: "ponere", answer: "plaatsen" },
        //{ id: 195, question: "filia", answer: "dochter" },
        //{ id: 196, question: "fata", answer: "lotsbeschikking" },
        //{ id: 197, question: "aperire", answer: "openen" },
        //{ id: 198, question: "ornare", answer: "versieren" },
        //{ id: 199, question: "sugere", answer: "opstaan" },
        //{ id: 200, question: "umbra", answer: "schim" },
        //{ id: 201, question: "liberare", answer: "bevrijden" },
        //{ id: 202, question: "coniunx", answer: "echtgenoot" },
        //{ id: 203, question: "custos", answer: "bewaker" },
        //{ id: 204, question: "caedere", answer: "doden" },
        //{ id: 205, question: "omnia", answer: "alle" },
        // I
        { id: 206, question: "esse", answer: "zijn" },
        { id: 207, question: "non", answer: "niet" },
        { id: 208, question: "enim", answer: "want" },
        { id: 209, question: "et", answer: "en" },
        { id: 210, question: "cur", answer: "waarom" },
        { id: 211, question: "quoque", answer: "ook" },
        { id: 212, question: "sed", answer: "maar" },
        { id: 213, question: "neque neque", answer: "noch noch" },
        { id: 214, question: "audire", answer: "horen" },
        { id: 215, question: "omnis", answer: "geheel" },
        // II
        { id: 216, question: "omnes, omnia", answer: "allen, alles" },
        { id: 217, question: "ubi", answer: "waar" },
        { id: 218, question: "femina", answer: "vrouw" },
        { id: 219, question: "autem", answer: "echter" },
        { id: 220, question: "tum", answer: "dan" },
        { id: 221, question: "dicere", answer: "zeggen" },
        { id: 222, question: "novus", answer: "nieuw" },
        { id: 223, question: "navis", answer: "schip" },
        { id: 224, question: "mare", answer: "zee" },
        { id: 225, question: "stare", answer: "staan" },
        // III
        //{ id: 226, question: "etiam", answer: "ook" },
        //{ id: 227, question: "nam", answer: "want" },
        //{ id: 228, question: "servus", answer: "slaaf" },
        //{ id: 229, question: "serva", answer: "slavin" },
        //{ id: 230, question: "videre", answer: "zien" },
        //{ id: 231, question: "dea", answer: "godin" },
        //{ id: 232, question: "mater", answer: "moeder" },
        //{ id: 233, question: "urbs", answer: "stad" },
        //{ id: 234, question: "quid", answer: "wat" },
        //{ id: 235, question: "facere", answer: "doen" },
        //// IV
        //{ id: 236, question: "iam", answer: "al" },
        //{ id: 237, question: "in +acc", answer: "in" },
        //{ id: 238, question: "in +abl", answer: "in" },
        //{ id: 239, question: "ad +acc", answer: "naar" },
        //{ id: 240, question: "deus", answer: "god" },
        //{ id: 241, question: "magnus", answer: "groot" },
        //{ id: 242, question: "ita", answer: "zo" },
        //{ id: 243, question: "ibi", answer: "daar" },
        //{ id: 244, question: "posse", answer: "kunnen" },
        //{ id: 245, question: "caput", answer: "hoofd" },
        //// V
        //{ id: 246, question: "vocare", answer: "roepen" },
        //{ id: 247, question: "venire", answer: "komen" },
        //{ id: 248, question: "-ne", answer: "achtervoegsel voor vraagzin" },
        //{ id: 249, question: "quis", answer: "wie" },
        //{ id: 250, question: "vos", answer: "jullie" },
        //{ id: 251, question: "is, ea, id", answer: "die, deze" },
        //{ id: 252, question: "tu", answer: "jij" },
        //{ id: 253, question: "ego", answer: "ik" },
        //{ id: 254, question: "homo", answer: "man" },
        //{ id: 255, question: "vir", answer: "man" },
        //// VI
        //{ id: 256, question: "filius", answer: "zoon" },
        //{ id: 257, question: "ire", answer: "gaan" },
        //{ id: 258, question: "ferre", answer: "dragen" },
        //{ id: 259, question: "nunc", answer: "nu" },
        //{ id: 260, question: "petere", answer: "opzoeken" },
        //{ id: 261, question: "amor", answer: "liefde" },
        //{ id: 262, question: "mons", answer: "berg" },
        //{ id: 263, question: "inter +acc", answer: "tussen" },
        //{ id: 264, question: "-que", answer: "en" },
        //{ id: 265, question: "alii..alii", answer: "sommigen anderen" },
        //// VII
        //{ id: 266, question: "dare", answer: "geven" },
        //{ id: 267, question: "movere", answer: "bewegen" },
        //{ id: 268, question: "post +acc", answer: "na" },
        //{ id: 269, question: "nox", answer: "nacht" },
        //{ id: 270, question: "multus", answer: "veel" },
        //{ id: 271, question: "nos", answer: "wij" },
        //{ id: 272, question: "habere", answer: "hebben" },
        //{ id: 273, question: "pater", answer: "vader" },
        //{ id: 274, question: "sic", answer: "zo" },
        //{ id: 275, question: "cognoscere", answer: "leren kennen" },
        //// VIII
        //{ id: 276, question: "cupere", answer: "willen" },
        //{ id: 277, question: "tamen", answer: "toch" },
        //{ id: 278, question: "capere", answer: "innemen" },
        //{ id: 279, question: "ceteri", answer: "overige" },
        //{ id: 280, question: "a, ab +abl", answer: "vanaf" },
        //{ id: 281, question: "de +abl", answer: "vanaf" },
        //{ id: 282, question: "an", answer: "of" },
        //{ id: 283, question: "ducere", answer: "leiden" },
        //{ id: 284, question: "cum +abl", answer: "samen met" },
        //{ id: 285, question: "cum +ind", answer: "wanneer" },
        //// IX
        //{ id: 286, question: "e, ex +abl", answer: "uit" },
        //{ id: 287, question: "credere", answer: "geloven" },
        //{ id: 288, question: "numquam", answer: "nooit" },
        //{ id: 289, question: "miles", answer: "soldaat" },
        //{ id: 290, question: "ecce", answer: "kijk" },
        //{ id: 291, question: "sine +abl", answer: "zonder" },
        //{ id: 292, question: "mors", answer: "(de) dood" },
        //{ id: 293, question: "modus", answer: "manier" },
        //{ id: 294, question: "tandem", answer: "eindelijk" },
        //{ id: 295, question: "ille, illa, illud", answer: "hij, zij, het" },
        //// X
        //{ id: 296, question: "atque, ac", answer: "en" },
        //{ id: 297, question: "bonus", answer: "goed" },
        //{ id: 298, question: "unus", answer: "één" },
        //{ id: 299, question: "tenere", answer: "vasthouden" },
        //{ id: 300, question: "meus", answer: "mijn" },
        //{ id: 301, question: "os", answer: "mond" },
        //{ id: 302, question: "hic", answer: "hier" },
        //{ id: 303, question: "ipse, ipsa, ipsum", answer: "zelf" },
        //{ id: 304, question: "suus", answer: "zijn, haar, hun" },
        //{ id: 305, question: "noster", answer: "ons, onze" },
        //// XI
        //{ id: 306, question: "nullus", answer: "geen" },
        //{ id: 307, question: "hic, haec, hoc", answer: "hij, zij, het" },
        //{ id: 308, question: "vester", answer: "jullie" },
        //{ id: 309, question: "longus", answer: "lang" },
        //{ id: 310, question: "vale", answer: "vaarwel" },
        //{ id: 311, question: "solus", answer: "alleen" },
        //{ id: 312, question: "tuus", answer: "jouw" },
        //{ id: 313, question: "adhuc", answer: "nog" },
        //{ id: 314, question: "num", answer: "toch zeker niet" },
        //{ id: 315, question: "semper", answer: "altijd" },
        //// XII
        //{ id: 316, question: "duo", answer: "twee" },
        //{ id: 317, question: "causa", answer: "reden" },
        //{ id: 318, question: "adesse", answer: "aanwezig zijn" },
        //{ id: 319, question: "ut", answer: "zoals" },
        //{ id: 320, question: "aqua", answer: "water" },
        //{ id: 321, question: "dux", answer: "leider" },
        //{ id: 322, question: "malus", answer: "slecht" },
        //{ id: 323, question: "totus", answer: "geheel" },
        //{ id: 324, question: "tunc", answer: "dan" },
        //{ id: 325, question: "nemo", answer: "niemand" },
        //// XIII
        //{ id: 326, question: "pro +abl", answer: "voor" },
        //{ id: 327, question: "quia", answer: "omdat" },
        //{ id: 328, question: "quod", answer: "omdat" },
        //{ id: 329, question: "nisi", answer: "als niet" },
        //{ id: 330, question: "dum", answer: "terwijl" },
        //{ id: 331, question: "si", answer: "als" },
        //{ id: 332, question: "postquam", answer: "nadat" },
        //{ id: 333, question: "iste, ista, istud", answer: "hij, zij, het" },
        //{ id: 334, question: "sicut", answer: "zoals" },
        //{ id: 335, question: "qui, quae, quod", answer: "die, dat, wie)" },
        ];

    // Create a shuffled version of the flashcards
    let shuffledCards = [];

    // Fisher-Yates shuffle algorithm function
    function shuffleArray(array: any) {
        // Create a copy of the original array to avoid modifying it
        const arrayCopy = [...array];
        // Start from the last element and swap it with a randomly selected element
        for (let i = arrayCopy.length - 1; i > 0; i--) {
            // Pick a random index from 0 to i
            const j = Math.floor(Math.random() * (i + 1));
            // Swap elements at i and j
            [arrayCopy[i], arrayCopy[j]] = [arrayCopy[j], arrayCopy[i]];
        }
        return arrayCopy;
    }

    // Initialize shuffled cards when component loads
    shuffledCards = shuffleArray(flashCards);

    // Keep track of the current card index
    let currentCardIndex = 0;

    // State for tracking points system
    let points = 0;
    let attempted = 0;

    // Function to go to the next card
    // Function to go to the next card
    function nextCard() {
        if (currentCardIndex < shuffledCards.length - 1) {
            currentCardIndex++;
        }
    }

    // Function to go to the previous card
    function prevCard() {
        if (currentCardIndex > 0) {
            currentCardIndex--;
        }
    }
    // Function to update points when an answer is submitted
    function handleAnswerSubmit(event: any) {
        const isCorrect = event.detail.isCorrect;
        attempted++;

        if (isCorrect) {
            points++; // Add 1 point for correct answer

            // Set a 2-second delay for correct answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 2000);
            }
        } else {
            // No point deduction for incorrect answers

            // Set a 5-second delay for incorrect answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 5000);
            }
        }
    }
</script>

<main>
    <div class="container">
        <h1>Flash Cards Latijn</h1>

        <div class="score-container">
            <p>Points: {points} (Attempted: {attempted})</p>
        </div>

        <div class="card-container">
            <FlashCard
                flashCard={shuffledCards[currentCardIndex]}
                on:answerSubmitted={handleAnswerSubmit}
            />
        </div>

        <div class="navigation">
            <button on:click={prevCard} disabled={currentCardIndex === 0}
                >Previous</button
            >
            <span class="card-counter"
                >{currentCardIndex + 1} / {shuffledCards.length}</span
            >
            <button
                on:click={nextCard}
                disabled={currentCardIndex === shuffledCards.length - 1}
                >Next</button
            >
        </div>
    </div>
</main>

<style>
    :global(body) {
        background-color: #10abb4;
        color: #004c50;
        margin: 0;
        padding: 0;
        font-family:
            -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans,
            Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: white;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 76, 80, 0.1);
    }

    h1 {
        color: #004c50;
        margin-bottom: 20px;
        font-weight: 700;
        text-align: center;
    }

    .score-container {
        margin-bottom: 20px;
        font-size: 1.2rem;
        font-weight: bold;
        color: #004c50;
        background-color: rgba(16, 171, 180, 0.1);
        padding: 8px 16px;
        border-radius: 8px;
    }

    .card-container {
        width: 100%;
        margin-bottom: 20px;
    }

    .navigation {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 400px;
        padding: 10px;
        background-color: rgba(0, 147, 156, 0.05);
        border-radius: 8px;
    }

    button {
        background-color: #00939c;
        color: white;
        border: none;
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 4px;
        transition: all 0.3s ease;
        font-weight: 500;
        box-shadow: 0 2px 4px rgba(0, 76, 80, 0.2);
    }

    button:hover {
        background-color: #10abb4;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 76, 80, 0.3);
    }

    button:disabled {
        background-color: rgba(0, 147, 156, 0.3);
        cursor: not-allowed;
        box-shadow: none;
        transform: none;
    }

    .card-counter {
        font-size: 1rem;
        color: #502000;
        font-weight: 600;
        background-color: rgba(156, 62, 0, 0.1);
        padding: 4px 10px;
        border-radius: 4px;
    }
</style>
