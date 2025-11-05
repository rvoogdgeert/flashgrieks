<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        //// A
        //{ id: 1, question: "οὐ, οὐκ, οὐχ", answer: "niet" },
        //{ id: 2, question: "εἰμι", answer: "zijn" },
        //{ id: 3, question: "ἄνθρωπος, ὁ", answer: "mens" },
        //{ id: 4, question: "θεός, ο/ἡ", answer: "god" },
        //{ id: 5, question: "δουλος", answer: "slaaf" },
        //{ id: 6, question: "τί;", answer: "wat" },
        //{ id: 7, question: "ἔχω", answer: "hebben" },
        //{ id: 8, question: "δε, δ'", answer: "en" },
        //{ id: 9, question: "φέρω", answer: "dragen" },
        //{ id: 10, question: "βαίνω", answer: "gaan" },

        //// B
        //{ id: 11, question: "προς", answer: "naar" },
        //{ id: 12, question: "ἀλλά, ἀλλ'", answer: "maar" },
        //{ id: 13, question: "οὕτως", answer: "zo" },
        //{ id: 14, question: "νῦν", answer: "nu" },
        //{ id: 15, question: "εἰς", answer: "naar" },
        //{ id: 16, question: "καί", answer: "en" },
        //{ id: 17, question: "λαμβάνω", answer: "nemen" },
        //{ id: 18, question: "ποιέω", answer: "doen" },
        //{ id: 19, question: "γάρ", answer: "want" },
        //{ id: 20, question: "φίλος, ὁ", answer: "vriend" },

        //// Γ
        //{ id: 21, question: "ἐνταῦθα", answer: "daar" },
        //{ id: 22, question: "μέγας", answer: "groot" },
        //{ id: 23, question: "μέν", answer: "niet vertalen" },
        //{ id: 24, question: "ἔπειτα", answer: "vervolgens" },
        //{ id: 25, question: "οὐδέν", answer: "niets" },
        //{ id: 26, question: "ἄλλος", answer: "ander" },
        //{ id: 27, question: "ἕκαστος", answer: "ieder" },
        //{ id: 28, question: "μάλα", answer: "zeer" },
        //{ id: 29, question: "καλός", answer: "mooi" },
        //{ id: 30, question: "οὖν", answer: "dus" },

        //// Δ
        //{ id: 31, question: "ἔγω", answer: "ik" },
        //{ id: 32, question: "ἐπί", answer: "bij" },
        //{ id: 33, question: "πολύς", answer: "veel" },
        //{ id: 34, question: "ἐν", answer: "in" },
        //{ id: 35, question: "οἰκία, ἡ", answer: "huis" },
        //{ id: 36, question: "λέγω", answer: "zeggen" },
        //{ id: 37, question: "ἐνθάδε", answer: "hierheen" },
        //{ id: 38, question: "ἥκω", answer: "komen" },
        //{ id: 39, question: "ὅτι", answer: "dat" },

        //// Ε
        //{ id: 40, question: "κακός", answer: "slecht" },
        //{ id: 41, question: "μετά", answer: "met" },
        //{ id: 42, question: "ἵππος, ὁ", answer: "paard" },
        //{ id: 43, question: "ἐκ", answer: "uit" },
        //{ id: 44, question: "ἄγω", answer: "brengen" },
        //{ id: 45, question: "λόγος, ὁ", answer: "woord" },
        //{ id: 46, question: "ἐξεστι(ν)", answer: "het is mogelijk voor" },
        //{ id: 47, question: "ἐπί", answer: "bij" },
        //{ id: 48, question: "τότε", answer: "dan" },
        //{ id: 49, question: "διά", answer: "door" },

        // Ζ
        { id: 50, question: "μετά", answer: "na" },
        { id: 51, question: "χρόνος, ὁ", answer: "tijd" },
        { id: 52, question: "ὑιος, ὁ", answer: "zoon" },
        { id: 53, question: "εἰ", answer: "als" },
        { id: 54, question: "ἡμέρα, ἡ", answer: "dag" },
        { id: 54, question: "ακουω", answer: "horen" },
        { id: 56, question: "ὑμεῖς", answer: "jullie" },
        { id: 58, question: "ἡμεῖς", answer: "wij" },
        { id: 59, question: "ὧδε", answer: "zo" },

        // Η
        { id: 60, question: "μη", answer: "niet" },
        { id: 60, question: "μονος", answer: "alleen" },
        { id: 61, question: "προς", answer: "bij" },
        { id: 62, question: "θαλαττα, η", answer: "zee" },
        { id: 62, question: "ἀνεμος, ο", answer: "wind" },
        { id: 62, question: "αὐτος", answer: "hij" },
        { id: 63, question: "παρθενος, ἡ", answer: "meisje" },
        { id: 64, question: "οὐδείς", answer: "niemand" },
        { id: 65, question: "eπι", answer: "op" },
        { id: 66, question: "πολυς", answer: "veel" },

        // Θ
        { id: 67, question: "ὥσπερ", answer: "zoals" },
        { id: 68, question: "ὅσπερ", answer: "altijd" },
        { id: 69, question: "μετά ταῦτα", answer: "daarna" },
        { id: 70, question: "ἀπο", answer: "vanaf" },
        { id: 71, question: "ἀποθνήσκω", answer: "sterven" },
        { id: 72, question: "τίς;", answer: "wie" },
        { id: 73, question: "περί", answer: "om" },
        { id: 74, question: "θάνατος, ὁ", answer: "dood" },
        { id: 75, question: "παρείμι", answer: "aanwezig zijn" },
        { id: 76, question: "ὅδε", answer: "deze" },

        // Ι
        { id: 77, question: "οὐδέ", answer: "en niet" },
        { id: 78, question: "πατήρ, ὁ", answer: "vader" },
        { id: 79, question: "οὐδέν", answer: "niets" },
        { id: 80, question: "ηδη", answer: "al" },
        { id: 81, question: "οὐκέτι", answer: "niet meer" },
        { id: 82, question: "πᾶς", answer: "geheel"},
        { id: 83, question: "σῶμα, το", answer: "lichaam" },
        { id: 84, question: "παῖς, ὁ/ἡ", answer: "kind" },
        { id: 85, question: "οἷος τε εἰμί", answer: "in staat zijn" },
        { id: 86, question: "γυνή, ἡ", answer: "vrouw" },

        //// Κ
        //{ id: 87, question: "ὑμετέρος", answer: "uw" },
        //{ id: 88, question: "ὑμετέρος", answer: "onze" },
        //{ id: 89, question: "μητήρ, ἡ", answer: "moeder" },
        //{ id: 90, question: "ὀλίγος", answer: "weinig" },
        //{ id: 91, question: "μετά", answer: "zeer" },
        //{ id: 92, question: "εὖ", answer: "goed" },
        //{ id: 93, question: "πόλις, ἡ", answer: "stad" },
        //{ id: 94, question: "κατά", answer: "van af" },

        //// 6A
        //{ id: 50, question: "τὸ τέκνον", answer: "kind" },
        //{ id: 51, question: "λείπω", answer: "laten" },
        //{ id: 52, question: "αἱ Ἀθῆναι", answer: "Athene" },
        //{ id: 53, question: "τὸ πλοῖον", answer: "schip" },
        //{ id: 54, question: "ἡ νῆσος", answer: "eiland" },
        //{ id: 55, question: "πλέω", answer: "varen" },
        //{ id: 56, question: "διά", answer: "door" },
        //{ id: 57, question: "ἡ λύπη", answer: "verdriet" },
        //{ id: 58, question: "μετά", answer: "na" },
        //{ id: 59, question: "ὁ χρόνος", answer: "tijd" },
        //{ id: 60, question: "Ἀθηναῖος", answer: "Atheens" },
        //{ id: 61, question: "ὁ Ἀθηναῖος", answer: "Athener" },
        //{ id: 62, question: "σῴζω", answer: "redden" },
        //{ id: 63, question: "ὁ υἱός", answer: "zoon" },
        //{ id: 64, question: "εἰμί", answer: "ik ben" },
        //{ id: 65, question: "εἰ", answer: "als" },
        //{ id: 66, question: "ἐμέ με", answer: "mij" },
        //{ id: 67, question: "γαμέω", answer: "trouwen" },
        //{ id: 68, question: "ὁ γάμος", answer: "huwelijk" },
        //{ id: 69, question: "χαίρω", answer: "blij zijn" },
        ////6B
        //{ id: 70, question: "αὐτοῖς", answer: "hen" },
        //{ id: 71, question: "ἡ θύρα", answer: "deur" },
        //{ id: 72, question: "πάλιν", answer: "weer" },
        //{ id: 73, question: "ἡ ἡμέρα", answer: "dag" },
        //{ id: 74, question: "ἀκούω", answer: "horen" },
        //{ id: 75, question: "μου ἐμοῦ", answer: "mij" },
        //{ id: 76, question: "μένω", answer: "blijven" },
        //{ id: 77, question: "μένω", answer: "wachten" },
        //{ id: 78, question: "ὑμεῖς", answer: "jullie" },
        //{ id: 79, question: "δή", answer: "dan" },
        //{ id: 80, question: "δακρύω", answer: "huilen" },
        //{ id: 81, question: "ἡμεῖς", answer: "wij" },
        //{ id: 82, question: "εἶναι", answer: "zijn" },
        //{ id: 83, question: "ὧδε", answer: "zo" },
        //{ id: 84, question: "θαυμάζω ὅτι", answer: "zich erover verwonderen dat" },
        //{ id: 85, question: "μή", answer: "niet" },
        //{ id: 86, question: "μόνος", answer: "alleen" },
        //{ id: 87, question: "πρός", answer: "bij" },
        //// 6C
        //{ id: 88, question: "καθεύδω", answer: "slapen" },
        //{ id: 89, question: "αἴρω", answer: "optillen" },
        //{ id: 90, question: "ἡ βία", answer: "kracht" },
        //{ id: 91, question: "ἡ ἀνδρεία", answer: "moed" },
        //{ id: 92, question: "ἡμᾶς", answer: "ons" },
        //{ id: 93, question: "ἔξω", answer: "buiten" },
        //{ id: 94, question: "ἡμῖν", answer: "ons" },
        //{ id: 95, question: "ἐκβαίνω", answer: "gaan uit" },
        //{ id: 96, question: "σωτηρία", answer: "redding" },
        //{ id: 97, question: "ἡ θάλαττα", answer: "zee" },
        //{ id: 98, question: "εἰσβαίνω", answer: "ingaan" },
        //{ id: 99, question: "ὁ ἄνεμος", answer: "wind" },
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
