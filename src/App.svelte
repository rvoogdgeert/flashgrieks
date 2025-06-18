<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        //{
        //id: 1,
        //question: "οὐ, οὐκ, οὐχ",
        //answer: "niet",
        //},
        //{
        //id: 2,
        //question: "ἐστί(ν)",
        //answer: "is",
        //},
        //{
        //id: 3,
        //question: "ὁ ἄνθρωπος",
        //answer: "mens",
        //},
        //{
        //id: 4,
        //question: "ὁ θεός",
        //answer: "god",
        //},
        //{
        //id: 5,
        //question: "εἰσί(ν)",
        //answer: "zijn",
        //},
        //{
        //id: 6,
        //question: "ὁ δοῦλος",
        //answer: "slaaf",
        //},
        //{
        //id: 7,
        //question: "ἔχει",
        //answer: "heeft",
        //},
        //{
        //id: 8,
        //question: "ἔχουσι(ν)",
        //answer: "hebben",
        //},
        //{
        //id: 9,
        //question: "ἡ χώρα",
        //answer: "land",
        //},
        //{
        //id: 10,
        //question: "οἰκεῖ",
        //answer: "woont",
        //},
        //{
        //id: 11,
        //question: "οἰκοῦσι(ν)",
        //answer: "wonen",
        //},
        //{
        //id: 12,
        //question: "ὁ φόβος",
        //answer: "angst",
        //},
        //{
        //id: 13,
        //question: "δε, δ᾽",
        //answer: "en",
        //},
        //{
        //id: 14,
        //question: "φέρει",
        //answer: "draagt",
        //},
        //{
        //id: 15,
        //question: "φέρουσι(ν)",
        //answer: "dragen",
        //},
        //{
        //id: 16,
        //question: "τὸ θηρίον",
        //answer: "wild dier",
        //},
        //{
        //id: 17,
        //question: "βαίνει",
        //answer: "gaat",
        //},
        //{
        //id: 18,
        //question: "βαίνουσι(ν)",
        //answer: "gaan",
        //},
        //{
        //id: 19,
        //question: "πρός",
        //answer: "naar",
        //},
        //{
        //id: 20,
        //question: "αλλα, αλλ᾽",
        //answer: "maar",
        //},
        //{
        //id: 21,
        //question: "οὕτως, οὕτω",
        //answer: "zo",
        //},
        //{
        //id: 22,
        //question: "φεύγει",
        //answer: "vlucht",
        //},
        //{
        //id: 23,
        //question: "φεύγουσι(ν)",
        //answer: "vluchten",
        //},
        //{
        //id: 24,
        //question: "μάχη",
        //answer: "gevecht",
        //},
        //{
        //id: 25,
        //question: "νῦν",
        //answer: "nu",
        //},
        //{
        //id: 26,
        //question: "εἰς",
        //answer: "naar",
        //},
        //{
        //id: 27,
        //question: "καί",
        //answer: "en",
        //},
        //{
        //id: 28,
        //question: "λαμβάνει",
        //answer: "neemt",
        //},
        //{
        //id: 29,
        //question: "λαμβάνουσι(ν)",
        //answer: "nemen",
        //},

        //{
        //id: 30,
        //question: "τοῦτο",
        //answer: "dit",
        //},
        //{
        //id: 31,
        //question: "ποιεῖ",
        //answer: "doet",
        //},
        //{
        //id: 32,
        //question: "ποιοῦσι(ν)",
        //answer: "doen",
        //},
        //{
        //id: 33,
        //question: "ὁ δεσπότης",
        //answer: "heerser",
        //},
        //{
        //id: 34,
        //question: "γάρ",
        //answer: "want",
        //},
        //{
        //id: 35,
        //question: "ὁ φίλος",
        //answer: "vriend",
        //},
        //{
        //id: 36,
        //question: "ἐνθαῦτα",
        //answer: "daar",
        //},
        //{
        //id: 37,
        //question: "μέγας, μεγάλη, μέγα",
        //answer: "groot",
        //},
        //{
        //id: 38,
        //question: "δεινός, δεινή, δεινόν",
        //answer: "verschrikkelijk",
        //},
        //{
        //id: 39,
        //question: "φοβερός, φοβερά, φοβερόν",
        //answer: "angstaanjagend",
        //},
        //{
        //id: 40,
        //question: "μέν",
        //answer: "tweede zin",
        //},
        //{
        //id: 41,
        //question: "κεφαλή",
        //answer: "hoofd",
        //},
        //{
        //id: 42,
        //question: "θνητός",
        //answer: "sterfelijk",
        //},
        //{
        //id: 43,
        //question: "ἀθάνατος",
        //answer: "onsterfelijk",
        //},
        //{
        //id: 44,
        //question: "ζητεῖ",
        //answer: "zoekt",
        //},
        //{
        //id: 45,
        //question: "εὑρίσκει",
        //answer: "vindt",
        //},
        //{
        //id: 46,
        //question: "μακρός, μακρά, μακρόν",
        //answer: "lang",
        //},
        //{
        //id: 47,
        //question: "ἔπειτα",
        //answer: "daarna",
        //},
        //{
        //id: 48,
        //question: "οὐδέν",
        //answer: "niets",
        //},
        //{
        //id: 49,
        //question: "μία",
        //answer: "een",
        //},
        //{
        //id: 50,
        //question: "τί...",
        //answer: "waarom",
        //},
        //{
        //id: 51,
        //question: "πρῶτον μέν..., ἔπειτα δέ",
        //answer: "eerst daarna",
        //},
        //{
        //id: 52,
        //question: "ἀποκτείνει",
        //answer: "doodt",
        //},
        //{
        //id: 53,
        //question: "καλεῖ",
        //answer: "roept",
        //},
        //{
        //id: 54,
        //question: "νέος, νέα, νέον",
        //answer: "nieuw",
        //},
        //{
        //id: 55,
        //question: "ἄλλος, ἄλλη, ἄλλο",
        //answer: "ander",
        //},
        //{
        //id: 56,
        //question: "ἕκαστος, ἑκάστη, ἕκαστον",
        //answer: "ieder",
        //},
        //{
        //id: 57,
        //question: "αὐτίκα",
        //answer: "meteen",
        //},
        //{
        //id: 58,
        //question: "ἡ πέτρα",
        //answer: "rots",
        //},
        //{
        //id: 59,
        //question: "κρύπτει",
        //answer: "verbergt",
        //},
        // 5A
        //{
        //    id: 60,
        //    question: "ἡ βασίλεια",
        //    answer: "koningin",
        //},
        //{
        //    id: 61,
        //    question: "μάλα",
        //    answer: "erg",
        //},
        //{
        //    id: 62,
        //    question: "ἀνδρεῖος",
        //    answer: "dapper",
        //},
        //{
        //    id: 63,
        //    question: "καλός",
        //    answer: "mooi",
        //},
        //{
        //    id: 64,
        //    question: "τὸ δῶρον",
        //    answer: "geschenk",
        //},
        //{
        //    id: 65,
        //    question: "ὁ πόλεμος",
        //    answer: "oorlog",
        //},
        //{
        //    id: 66,
        //    question: "φιλέω",
        //    answer: "houden van",
        //},
        //{
        //    id: 67,
        //    question: "φίλος",
        //    answer: "geliefd",
        //},
        //{
        //    id: 68,
        //    question: "θαυμάζω",
        //    answer: "bewonderen",
        //},
        //{
        //    id: 69,
        //    question: "οὖν",
        //    answer: "dan",
        //},
        //{
        //    id: 70,
        //    question: "αἰτέω",
        //    answer: "vragen",
        //},
        //{
        //    id: 71,
        //    question: "ἐγώ",
        //    answer: "ik",
        //},
        //{
        //    id: 72,
        //    question: "ἐπιθυμέω",
        //    answer: "verlangen",
        //},
        //{
        //    id: 73,
        //    question: "ἐθέλω",
        //    answer: "willen",
        //},
        //{
        //    id: 74,
        //    question: "σύ",
        //    answer: "jij",
        //},
        //{
        //    id: 75,
        //    question: "ἐπί",
        //    answer: "op af",
        //},
        //{
        //    id: 76,
        //    question: "πέμπω",
        //    answer: "sturen",
        //},
        //{
        //    id: 77,
        //    question: "ὁ ἑταῖρος",
        //    answer: "vriend",
        //},
        //{
        //    id: 78,
        //    question: "πολλοί",
        //    answer: "veel",
        //},
        // 5B
        { id: 79,  question: "ἐν", answer: "in" },
        { id: 80,  question: "ἡ οἰκία", answer: "huis" },
        { id: 81,  question: "...τε καί...", answer: "en" },
        { id: 82,  question: "αὐτῷ", answer: "hem" },
        { id: 83,  question: "λέγω", answer: "zeggen" },
        { id: 84,  question: "ἐνθάδε", answer: "hierheen" },
        { id: 85,  question: "ἥκω", answer: "komen" },
        { id: 86,  question: "αὐτῇ", answer: "haar" },
        { id: 87,  question: "ὅτι", answer: "dat" },
        { id: 88,  question: "σέ",  answer: "jou" },
        { id: 89,  question: "σός",  answer: "jouw" },
        { id: 90,  question: "μοί",  answer: "mij" },
        { id: 91,  question: "παρέχω",  answer: "verschaffen" },
        { id: 92,  question: "λύω",  answer: "losmaken" },
        { id: 93,  question: "ἡ θεός",  answer: "godin" },
        { id: 94,  question: "ὅμοιος",  answer: "gelijk aan" },
        { id: 95,  question: "ὁ ξένος",  answer: "vreemdeling" },
        { id: 96,  question: "κακός",  answer: "slecht" },
        { id: 97,  question: "τὸ ἔργον",  answer: "daad" },
        { id: 98,  question: "μέλλω",  answer: "op het punt staan om" },
        { id: 99,  question: "αὐτήν",  answer: "haar" },
        { id: 100, question: "μέτα", answer: "met" },
        { id: 101, question: "τὰ ὅπλα", answer: "wapens" },
        { id: 102, question: "ὁ ἵππος", answer: "paard" },
        { id: 103, question: "αὐτῆς", answer: "haar" },
        // 5C
        { id: 104, question: "κελεύω", answer: "bevelen" },
        { id: 105, question: "εκ", answer: "uit" },
        { id: 106, question: "ἄγω", answer: "brengen" },
        { id: 107, question: "ὁ νεκρός", answer: "lijk" },
        { id: 108, question: "ὁ λόγος", answer: "woord" },
        { id: 109, question: "αὐτόν", answer: "hem" },
        { id: 110, question: "κρατέω", answer: "machten hebben over" },
        { id: 111, question: "εξεστι", answer: "het is mogelijk om" },
        { id: 112, question: "επι", answer: "bij" },
        { id: 113, question: "αἱ πύλαι", answer: "poort" },
        { id: 114, question: "αὐτοῦ", answer: "hem" },
        { id: 115, question: "τοτε", answer: "dan" },
        { id: 116, question: "ἰσχυρός", answer: "machtig" },
        //// 6A
        //{ id: 117, question: "τὸ τέκνον", answer: "kind" },
        //{ id: 118, question: "λείπω", answer: "verlaten" },
        //{ id: 119, question: "αἱ Ἀθῆναι", answer: "Athene" },
        //{ id: 120, question: "τὸ πλοῖον", answer: "schip" },
        //{ id: 121, question: "ἡ νῆσος", answer: "eiland" },
        //{ id: 122, question: "πλέω", answer: "varen" },
        //{ id: 123, question: "δια", answer: "door" },
        //{ id: 124, question: "ἡ λύπη", answer: "verdriet" },
        //{ id: 125, question: "μετα", answer: "na" },
        //// 6B
        //{ id: 126, question: "αὐτοῖς", answer: "hen" },
        //{ id: 127, question: "ἡ θύρα", answer: "deur" },
        //{ id: 128, question: "πάλιν", answer: "weer" },
        //{ id: 129, question: "ἡ ἡμέρα", answer: "dag" },
        //{ id: 130, question: "ἀκούω", answer: "horen" },
        //{ id: 131, question: "μοῦ, ἐμοῦ", answer: "mij, mijn" },
        //{ id: 132, question: "μένω", answer: "blijven" },
        //{ id: 133, question: "ὑμεῖς", answer: "jullie" },
        //{ id: 134, question: "δή", answer: "dan, dus" },
        //{ id: 135, question: "δακρύω", answer: "huilen" },
        //{ id: 136, question: "ἡμεῖς", answer: "wij" },
        //{ id: 137, question: "εἶναι", answer: "zijn" },
        //{ id: 138, question: "ὧδε", answer: "zo, als volgt" },
        //{ id: 139, question: "θαυμάζω ὅτι", answer: "zich erover verwonderen dat" },
        //{ id: 140, question: "μή", answer: "niet" },
        //{ id: 141, question: "μόνος", answer: "alleen" },
        //{ id: 142, question: "πρός", answer: "bij" },
        //// 6C
        //{ id: 143, question: "", answer: "" },
        //{ id: 144, question: "", answer: "" },
        //{ id: 145, question: "", answer: "" },
        //{ id: 146, question: "", answer: "" },
        //{ id: 147, question: "", answer: "" },
        //{ id: 148, question: "", answer: "" },
        //{ id: 149, question: "", answer: "" },

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
        <h1>Flash Cards Grieks</h1>

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
B
B
