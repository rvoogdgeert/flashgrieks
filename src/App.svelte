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

        //// Ζ
        //{ id: 50, question: "μετά", answer: "na" },
        //{ id: 51, question: "χρόνος, ὁ", answer: "tijd" },
        //{ id: 52, question: "ὑιος, ὁ", answer: "zoon" },
        //{ id: 53, question: "εἰ", answer: "als" },
        //{ id: 54, question: "ἡμέρα, ἡ", answer: "dag" },
        //{ id: 54, question: "ακουω", answer: "horen" },
        //{ id: 56, question: "ὑμεῖς", answer: "jullie" },
        //{ id: 58, question: "ἡμεῖς", answer: "wij" },
        //{ id: 59, question: "ὧδε", answer: "zo" },

        //// Η
        //{ id: 60, question: "μη", answer: "niet" },
        //{ id: 60, question: "μονος", answer: "alleen" },
        //{ id: 61, question: "προς", answer: "bij" },
        //{ id: 62, question: "θαλαττα, η", answer: "zee" },
        //{ id: 62, question: "ἀνεμος, ο", answer: "wind" },
        //{ id: 62, question: "αὐτος", answer: "hij" },
        //{ id: 63, question: "παρθενος, ἡ", answer: "meisje" },
        //{ id: 64, question: "οὐδείς", answer: "niemand" },
        //{ id: 65, question: "eπι", answer: "op" },
        //{ id: 66, question: "πολυς", answer: "veel" },

        //// Θ
        //{ id: 67, question: "ὥσπερ", answer: "zoals" },
        //{ id: 68, question: "ὅσπερ", answer: "altijd" },
        //{ id: 69, question: "μετά ταῦτα", answer: "daarna" },
        //{ id: 70, question: "ἀπο", answer: "vanaf" },
        //{ id: 71, question: "ἀποθνήσκω", answer: "sterven" },
        //{ id: 72, question: "τίς;", answer: "wie" },
        //{ id: 73, question: "περί", answer: "om" },
        //{ id: 74, question: "θάνατος, ὁ", answer: "dood" },
        //{ id: 75, question: "παρείμι", answer: "aanwezig zijn" },
        //{ id: 76, question: "ὅδε", answer: "deze" },

        //// Ι
        //{ id: 77, question: "οὐδέ", answer: "en niet" },
        //{ id: 78, question: "πατήρ, ὁ", answer: "vader" },
        //{ id: 79, question: "οὐδέν", answer: "niets" },
        //{ id: 80, question: "ηδη", answer: "al" },
        //{ id: 81, question: "οὐκέτι", answer: "niet meer" },
        //{ id: 82, question: "πᾶς", answer: "geheel"},
        //{ id: 83, question: "σῶμα, το", answer: "lichaam" },
        //{ id: 84, question: "παῖς, ὁ/ἡ", answer: "kind" },
        //{ id: 85, question: "οἷος τε εἰμί", answer: "in staat zijn" },
        //{ id: 86, question: "γυνή, ἡ", answer: "vrouw" },

        //// Κ
        //{ id: 87, question: "ὑμετέρος", answer: "uw" },
        //{ id: 88, question: "ὑμετέρος", answer: "onze" },
        //{ id: 89, question: "μητήρ, ἡ", answer: "moeder" },
        //{ id: 90, question: "ὀλίγος", answer: "weinig" },
        //{ id: 91, question: "μετά", answer: "zeer" },
        //{ id: 92, question: "εὖ", answer: "goed" },
        //{ id: 93, question: "πόλις, ἡ", answer: "stad" },
        //{ id: 94, question: "κατά", answer: "van af" },

       //// Λ
       //{ id: 95, question: "χωρα, ἡ", answer: "gebied" },
       //{ id: 96, question: "οἰκεω", answer: "wonen" },
       //{ id: 97, question: "φοβος, ὁ", answer: "angst" },
       //{ id: 98, question: "φευγω", answer: "vluchten" },
       //{ id: 99, question: "μαχη, ἡ", answer: "gevecht" },
       //{ id: 100, question: "δεσποτης, ὁ", answer: "heerser" },
       //{ id: 101, question: "δεινος", answer: "verschrikkelijk" },
       //{ id: 102, question: "θνητος", answer: "sterfelijk" },
       //{ id: 103, question: "ἀθανατος", answer: "onsterfelijk" },
       //{ id: 104, question: "ζητεω", answer: "zoeken" },

        //// Μ
        //{ id: 105, question: "εὑρισκω", answer: "vinden" },
        //{ id: 106, question: "μακρος", answer: "lang" },
        //{ id: 107, question: "ἀποκτεινω", answer: "doden" },
        //{ id: 108, question: "καλεω", answer: "roepen" },
        //{ id: 109, question: "νεος", answer: "nieuw" },
        //{ id: 110, question: "πετρα, ἡ", answer: "rots" },
        //{ id: 111, question: "κρυπτω", answer: "verbergen" },
        //{ id: 112, question: "πολεμος, ὁ", answer: "oorlog" },
        //{ id: 113, question: "φιλεω", answer: "houden van" },
        //{ id: 114, question: "φιλος", answer: "bevriend" },

        // Ν
        //{ id: 115, question: "θαυμαζω", answer: "bewonderen" },
        //{ id: 116, question: "αἰτεω", answer: "verzoeken" },
        //{ id: 117, question: "ἐπιθυμεω", answer: "verlangen" },
        //{ id: 118, question: "ἐθελω", answer: "willen" },
        //{ id: 119, question: "πεμπω", answer: "sturen" },
        //{ id: 120, question: "ἑταιρος, ὁ", answer: "vriend" },
        //{ id: 121, question: "παρεχω", answer: "verschaffen" },
        //{ id: 122, question: "λυω", answer: "losmaken" },
        //{ id: 123, question: "κελευω", answer: "bevelen" },
        //{ id: 124, question: "κρατεω +gen", answer: "overwinnen" },

        //// Ξ
        //{ id: 125, question: "τεκνον, το", answer: "kind" },
        //{ id: 126, question: "λειπω", answer: "verlaten" },
        //{ id: 127, question: "νησος, ἡ", answer: "eiland" },
        //{ id: 128, question: "πλεω", answer: "varen" },
        //{ id: 129, question: "γαμος, ὁ", answer: "huwelijk" },
        //{ id: 130, question: "χαιρεω +dat", answer: "blij zijn met" },
        //{ id: 131, question: "παλιν", answer: "weer" },
        //{ id: 132, question: "μενω", answer: "blijven" },
        //{ id: 133, question: "δακρυω", answer: "huilen" },
        //{ id: 134, question: "καθευδω", answer: "slapen" },

        //// Ο
        //{ id: 135, question: "αἰρω", answer: "optillen" },
        //{ id: 136, question: "βια, ἡ", answer: "geweld" },
        //{ id: 137, question: "ἀνδρεια, ἡ", answer: "moed" },
        //{ id: 138, question: "ἐξω", answer: "buiten" },
        //{ id: 139, question: "ἐκβαινω", answer: "gaan uit" },
        //{ id: 140, question: "εἰσβαινω", answer: "ingaan" },
        //{ id: 141, question: "μετεχω +gen", answer: "meedoen met" },
        //{ id: 142, question: "φυγη, ἡ", answer: "vlucht" },
        //{ id: 143, question: "ἱερος", answer: "heilig, gewijd aan" },
        //{ id: 144, question: "οἰνος, ὁ", answer: "wijn" },

        //// Π
        //{ id: 145, question: "κινδυνος, ὁ", answer: "gevaar" },
        //{ id: 146, question: "ἑαυτος", answer: "zichzelf" },
        //{ id: 147, question: "ἀποφερω", answer: "wegbrengen" },
        //{ id: 148, question: "νομιζω", answer: "menen, vinden" },
        //{ id: 149, question: "αἰτιος +gen", answer: "verantwoordelijk voor" },
        //{ id: 150, question: "ἡλιος, ὁ", answer: "zon" },
        //{ id: 151, question: "ὑπνος, ὁ", answer: "slaap" },
        //{ id: 152, question: "πλην +gen", answer: "behalve" },
        //{ id: 153, question: "φωνη, ἡ", answer: "stem" },
        //{ id: 154, question: "ἀνευ +gen", answer: "zonder" },

        ////// Ρ
        //{ id: 155, question: "ἀναβαινω", answer: "omhoog gaan" },
        //{ id: 156, question: "βλεπω", answer: "kijken" },
        //{ id: 157, question: "μονον", answer: "slechts" },
        //{ id: 158, question: "ἐμος", answer: "mijn" },
        //{ id: 159, question: "βιος, ὁ", answer: "leven" },
        //{ id: 160, question: "ῥιπτω", answer: "gooien" },
        //{ id: 161, question: "πιπτω", answer: "vallen" },
        //{ id: 162, question: "συμφορα, ἡ", answer: "gebeurtenis, ongeluk" },
        //{ id: 163, question: "φροντιζω +gen", answer: "zich zorgen maken over" },
        //{ id: 164, question: "στρατηγος, ὁ", answer: "legeraanvoerder" },

        ////// Σ
        //{ id: 165, question: "ναυτης, ὁ", answer: "zeeman" },
        //{ id: 166, question: "στρατιωτης, ὁ", answer: "soldaat" },
        //{ id: 167, question: "ἀνηρ, ὁ", answer: "man (gen: ἀνδρος)" },
        //{ id: 168, question: "εἰσφερω", answer: "naar binnen brengen" },
        //{ id: 169, question: "νους, ὁ", answer: "geest" },
        //{ id: 170, question: "παυω", answer: "tegenhouden, laten stoppen" },
        //{ id: 171, question: "κωλυω", answer: "verhinderen" },
        //{ id: 172, question: "ἁμα", answer: "tegelijkertijd" },
        //{ id: 173, question: "ἐχθρός", answer: "vijandig, gehaat" },
        //{ id: 174, question: "τυχη, ἡ", answer: "lot" },

        ////// Τ
        //{ id: 175, question: "ὁμως", answer: "toch" },
        //{ id: 176, question: "ἀγγελος, ὁ", answer: "bode" },
        //{ id: 177, question: "ἀληθεια, ἡ", answer: "waarheid" },
        //{ id: 178, question: "ἀγγελλω", answer: "melden" },
        //{ id: 179, question: "στρατια, ἡ", answer: "leger" },
        //{ id: 180, question: "πιστευω", answer: "vertrouwen" },
        //{ id: 181, question: "τοιουτος", answer: "zo'n, zodanig" },
        //{ id: 182, question: "ἀντι +gen", answer: "in plaats van" },
        //{ id: 183, question: "βοηθεω", answer: "helpen" },
        //{ id: 184, question: "καθιζω", answer: "(gaan) zitten" },

        ////// Υ
        //{ id: 185, question: "παλαιος", answer: "oud" },
        //{ id: 186, question: "ἐγγυς +gen", answer: "dicht bij" },
        //{ id: 187, question: "ἡγεμων, ὁ", answer: "leider (gen: ἡγεμονος)" },
        //{ id: 188, question: "εὐδαιμων", answer: "gelukkig" },
        //{ id: 189, question: "μηκετι", answer: "niet meer" },
        //{ id: 190, question: "ἀποπεμπω", answer: "wegsturen" },
        //{ id: 191, question: "ἐρις, ἡ", answer: "ruzie (gen: ἐρεως)" },
        //{ id: 192, question: "σωφρων", answer: "verstandig" },
        //{ id: 193, question: "ἀριστος", answer: "beste, zeer goed" },
        //{ id: 194, question: "σωτηρ, ὁ", answer: "redder (gen: σωτηρος)" },

        ////// Φ
        //{ id: 195, question: "λεων, ὁ", answer: "leeuw (gen: λεοντος)" },
        //{ id: 196, question: "χαιρε, χαιρετε", answer: "hallo" },
        //{ id: 197, question: "δευρο", answer: "hierheen" },
        //{ id: 198, question: "κομιζω", answer: "brengen, halen" },
        //{ id: 199, question: "σιτος, ὁ", answer: "voedsel" },
        //{ id: 200, question: "δειπνον, το", answer: "maaltijd" },
        //{ id: 201, question: "μελει +dat", answer: "het interesseert" },
        //{ id: 202, question: "πυρ, το", answer: "vuur (gen: πυρος)" },
        //{ id: 203, question: "πειθω", answer: "overtuigen" },
        //{ id: 204, question: "οἰκαδε", answer: "naar huis" },

        ////// Χ
        //{ id: 205, question: "ἀμφι +gen", answer: "om, rondom" },
        //{ id: 206, question: "πολεμεω", answer: "oorlog voeren" },
        //{ id: 207, question: "δοξα, ἡ", answer: "mening, roem" },
        //{ id: 208, question: "ἀποβαινω", answer: "weggaan" },
        //{ id: 209, question: "τικτω", answer: "baren" },
        //{ id: 210, question: "ἰσως", answer: "misschien" },
        //{ id: 211, question: "ἐλπιζω", answer: "hopen" },
        //{ id: 212, question: "τελευτη, ἡ", answer: "einde" },
        //{ id: 213, question: "προτερος", answer: "eerder, vroeger" },
        //{ id: 214, question: "ἀρχω +gen", answer: "leiden, heersen" },

        ////// Ψ
        //{ id: 215, question: "ἐλαυνω", answer: "voortdrijven" },
        //{ id: 216, question: "λαμπρος", answer: "schitterend" },
        //{ id: 217, question: "δακρυον, το", answer: "traan" },
        //{ id: 218, question: "θερμος", answer: "warm" },
        //{ id: 219, question: "καλυπτω", answer: "bedekken, verbergen" },
        //{ id: 220, question: "ἀμφοτεροι", answer: "beide(n)" },
        //{ id: 221, question: "χειρ, ἡ", answer: "hand (gen: χειρος)" },
        //{ id: 222, question: "προσωπον, το", answer: "gezicht" },
        //{ id: 223, question: "δουλη, ἡ", answer: "slavin" },
        //{ id: 224, question: "κλαιω, κλαω", answer: "huilen" },

        ////// Ω
        //{ id: 225, question: "μανθανω", answer: "leren, begrijpen, vernemen" },
        //{ id: 226, question: "ἀδικος", answer: "onrechtvaardig" },

        //// 6A
        //{ id: 227, question: "τὸ τέκνον", answer: "kind" },
        //{ id: 228, question: "λείπω", answer: "laten" },
        //{ id: 229, question: "αἱ Ἀθῆναι", answer: "Athene" },
        //{ id: 230, question: "τὸ πλοῖον", answer: "schip" },
        //{ id: 231, question: "ἡ νῆσος", answer: "eiland" },
        //{ id: 232, question: "πλέω", answer: "varen" },
        //{ id: 233, question: "διά", answer: "door" },
        //{ id: 234, question: "ἡ λύπη", answer: "verdriet" },
        //{ id: 235, question: "μετά", answer: "na" },
        //{ id: 236, question: "ὁ χρόνος", answer: "tijd" },
        //{ id: 237, question: "Ἀθηναῖος", answer: "Atheens" },
        //{ id: 238, question: "ὁ Ἀθηναῖος", answer: "Athener" },
        //{ id: 239, question: "σῴζω", answer: "redden" },
        //{ id: 240, question: "ὁ υἱός", answer: "zoon" },
        //{ id: 241, question: "εἰμί", answer: "ik ben" },
        //{ id: 242, question: "εἰ", answer: "als" },
        //{ id: 243, question: "ἐμέ με", answer: "mij" },
        //{ id: 244, question: "γαμέω", answer: "trouwen" },
        //{ id: 245, question: "ὁ γάμος", answer: "huwelijk" },
        //{ id: 246, question: "χαίρω", answer: "blij zijn" },
        ////6B
        //{ id: 247, question: "αὐτοῖς", answer: "hen" },
        //{ id: 248, question: "ἡ θύρα", answer: "deur" },
        //{ id: 249, question: "πάλιν", answer: "weer" },
        //{ id: 250, question: "ἡ ἡμέρα", answer: "dag" },
        //{ id: 251, question: "ἀκούω", answer: "horen" },
        //{ id: 252, question: "μου ἐμοῦ", answer: "mij" },
        //{ id: 253, question: "μένω", answer: "blijven" },
        //{ id: 254, question: "μένω", answer: "wachten" },
        //{ id: 255, question: "ὑμεῖς", answer: "jullie" },
        //{ id: 256, question: "δή", answer: "dan" },
        //{ id: 257, question: "δακρύω", answer: "huilen" },
        //{ id: 258, question: "ἡμεῖς", answer: "wij" },
        //{ id: 259, question: "εἶναι", answer: "zijn" },
        //{ id: 260, question: "ὧδε", answer: "zo" },
        //{ id: 261, question: "θαυμάζω ὅτι", answer: "zich erover verwonderen dat" },
        //{ id: 262, question: "μή", answer: "niet" },
        //{ id: 263, question: "μόνος", answer: "alleen" },
        //{ id: 264, question: "πρός", answer: "bij" },
        //// 6C
        //{ id: 265, question: "καθεύδω", answer: "slapen" },
        //{ id: 266, question: "αἴρω", answer: "optillen" },
        //{ id: 267, question: "ἡ βία", answer: "kracht" },
        //{ id: 268, question: "ἡ ἀνδρεία", answer: "moed" },
        //{ id: 269, question: "ἡμᾶς", answer: "ons" },
        //{ id: 270, question: "ἔξω", answer: "buiten" },
        //{ id: 271, question: "ἡμῖν", answer: "ons" },
        //{ id: 272, question: "ἐκβαίνω", answer: "gaan uit" },
        //{ id: 273, question: "σωτηρία", answer: "redding" },
        //{ id: 274, question: "ἡ θάλαττα", answer: "zee" },
        //{ id: 275, question: "εἰσβαίνω", answer: "ingaan" },
        //{ id: 276, question: "ὁ ἄνεμος", answer: "wind" },

        // Tekst 9B
        { id: 277, question: "χαῖρε, χαίρετε", answer: "gegroet" },
        { id: 278, question: "δεῦρο", answer: "hier" },
        { id: 279, question: "κομίζω", answer: "brengen" },
        { id: 280, question: "ὁ σῖτος", answer: "eten" },
        { id: 281, question: "τὸ δεῖπνον", answer: "maaltijd" },
        { id: 282, question: "μέλει μοι", answer: "het interesseert me" },
        { id: 283, question: "τὸ πῦρ (πυρός)", answer: "vuur" },
        { id: 284, question: "ἄξιος + gen.", answer: "waard" },
        { id: 285, question: "ὑμεῖς, ὑμῶν, ὑμῖν, ὑμᾶς", answer: "jullie" },
        { id: 286, question: "πείθω", answer: "overtuigen" },
        { id: 287, question: "ἐμοῦ, μου", answer: "mijn" },
        { id: 288, question: "ὑμέτερος", answer: "van jullie" },
        { id: 289, question: "ἡμέτερος", answer: "ons" },
        { id: 290, question: "ἡ μήτηρ (μητρός)", answer: "moeder" },
        { id: 291, question: "οἴκαδε", answer: "naar huis" },
        { id: 292, question: "σοί, σοι", answer: "voor jou" },
        { id: 293, question: "ἀμφί + acc.", answer: "rondom" },
        { id: 294, question: "πολεμέω", answer: "oorlog voeren" },
        { id: 295, question: "ἡ δόξα", answer: "mening" },
        { id: 296, question: "ἀποβαίνω", answer: "weggaan" },
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
