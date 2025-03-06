<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        {
            id: 1,
            question: "ου, ουκ, ουχ",
            answer: "niet",
        },
        {
            id: 2,
            question: "εστι(ν)",
            answer: "is",
        },
        {
            id: 3,
            question: "ο ανθρωπος",
            answer: "mens",
        },
        {
            id: 4,
            question: "ο θεος",
            answer: "god",
        },
        {
            id: 5,
            question: "εισι(ν)",
            answer: "zijn",
        },
        {
            id: 6,
            question: "ο δουλος",
            answer: "slaaf",
        },
        {
            id: 7,
            question: "εχει",
            answer: "heeft",
        },
        {
            id: 8,
            question: "εχουσι(ν)",
            answer: "hebben",
        },
        {
            id: 9,
            question: "η χωρα",
            answer: "land",
        },
        {
            id: 10,
            question: "οικει",
            answer: "woont",
        },
        {
            id: 11,
            question: "οικουσι(ν)",
            answer: "wonen",
        },
        {
            id: 12,
            question: "ο φοβος",
            answer: "angst",
        },
        {
            id: 13,
            question: "δε, δ᾽",
            answer: "en",
        },
        {
            id: 14,
            question: "φερει",
            answer: "draagt",
        },
        {
            id: 15,
            question: "φερουσι(ν)",
            answer: "dragen",
        },
        {
            id: 16,
            question: "το θηπριον",
            answer: "wild dier",
        },
        {
            id: 17,
            question: "βαινει",
            answer: "gaat",
        },
        {
            id: 18,
            question: "βαινουσι(ν)",
            answer: "gaan",
        },
        {
            id: 19,
            question: "προς",
            answer: "naar(toe)",
        },
        {
            id: 20,
            question: "αλλα, αλλ᾽",
            answer: "maar",
        },
        {
            id: 21,
            question: "ουτως, ουτω",
            answer: "zo",
        },
        {
            id: 22,
            question: "φευγει",
            answer: "vlucht",
        },
        {
            id: 23,
            question: "φευγουσι(ν)",
            answer: "vluchten",
        },
        {
            id: 24,
            question: "μαχη",
            answer: "gevecht",
        },
        {
            id: 25,
            question: "νυν",
            answer: "nu",
        },
        {
            id: 26,
            question: "εις",
            answer: "naar",
        },
        {
            id: 27,
            question: "και",
            answer: "en",
        },
        {
            id: 28,
            question: "λαμβανει",
            answer: "neemt",
        },
        {
            id: 29,
            question: "λαμβανουσι(ν)",
            answer: "nemen",
        },

        {
            id: 30,
            question: "τουτο",
            answer: "dit",
        },
        {
            id: 31,
            question: "ποιει",
            answer: "doet",
        },
        {
            id: 32,
            question: "ποιουσι(ν)",
            answer: "doen",
        },
        {
            id: 33,
            question: "ο δεσπωτης",
            answer: "heerser",
        },
        {
            id: 34,
            question: "γαρ",
            answer: "want",
        },
        {
            id: 35,
            question: "ο φιλος",
            answer: "vriend",
        },
        {
            id: 36,
            question: "ενθαυτα",
            answer: "daar",
        },
        {
            id: 37,
            question: "μεγας, μαγαλη, μεγα",
            answer: "groot",
        },
        {
            id: 38,
            question: "δεινος, δεινη, δεινον",
            answer: "verschrikkelijk",
        },
        {
            id: 39,
            question: "φοβερος, φοβερα, φεβερον",
            answer: "angstaanjagend",
        },
        {
            id: 40,
            question: "μεν",
            answer: "tweede zin",
        },
        {
            id: 41,
            question: "κεφαλη",
            answer: "hoofd",
        },
        {
            id: 42,
            question: "θνητος",
            answer: "sterfelijk",
        },
        {
            id: 43,
            question: "αθανατος",
            answer: "onsterfelijk",
        },
        {
            id: 44,
            question: "ζητει",
            answer: "zoekt",
        },
        {
            id: 45,
            question: "ευρισκει",
            answer: "vindt",
        },
        {
            id: 46,
            question: "μακρος, μακρα, μακρον",
            answer: "lang",
        },
        {
            id: 47,
            question: "επειτα",
            answer: "daarna",
        },
        {
            id: 48,
            question: "ουδεν",
            answer: "niets",
        },
        {
            id: 49,
            question: "μια",
            answer: "een",
        },
        {
            id: 50,
            question: "τι...",
            answer: "wat",
        },
        {
            id: 51,
            question: "πρωτον μεν..., επαιτα δε",
            answer: "eerst daarna",
        },
        {
            id: 52,
            question: "αποκτεινει",
            answer: "doodt",
        },
        {
            id: 53,
            question: "καλει",
            answer: "roept",
        },
        {
            id: 54,
            question: "νεος, νεα, νεον",
            answer: "nieuw",
        },
        {
            id: 55,
            question: "αλλοσ, αλλη, αλλο",
            answer: "ander",
        },
        {
            id: 56,
            question: "εκαστοσ, εκαστη, εκαστον",
            answer: "ieder",
        },
        {
            id: 57,
            question: "αυτικα",
            answer: "meteen",
        },
        {
            id: 58,
            question: "η πετρα",
            answer: "rots",
        },
        {
            id: 59,
            question: "κρυπτει",
            answer: "verbergt",
        },
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
            points--; // Subtract 1 point for incorrect answer

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
