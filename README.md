# d'en---dent---dans
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - Dans, D'en, Dent</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["dans", "d'en", "dent", "dans", "d'en", "dent", "dans", "d'en", "dent", "dans", "d'en", "dent", "dans", "d'en", "dent", "dans", "d'en", "dent", "dans", "dent"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✅ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "dans" indique une localisation (ex: dans la maison), "d'en" est une contraction de "de en" (ex: il parle d'en prendre), et "dent" est le nom de l'élément anatomique (ex: la dent de sagesse).`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "dans", "d'en" ou "dent"</h2>

    <p><strong>Règle :</strong> "Dans" indique une localisation (par exemple : "dans la maison"), "d'en" est la contraction de "de en" et s'utilise pour exprimer un rapport (par exemple : "il parle d'en prendre"), tandis que "dent" désigne l'élément anatomique présent dans la bouche (par exemple : "la dent de sagesse").</p>

    <form>
        <ol>
            <li>Il est parti ___ la pièce sans rien dire. <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>Il parlait ___ faire plus. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>J'ai une ___ qui me fait mal. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>Elle se cache souvent ___ sa chambre. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>J'ai besoin ___ acheter un peu plus. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>Le dentiste va examiner ma ___. <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>Il y a quelque chose ___ le sac. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>Il ne cesse ___ parler. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>Ma ___ bouge. <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>Je vais mettre cela ___ le tiroir. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>Il est important ___ discuter. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>J'ai perdu une ___. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>Elle a laissé son téléphone ___ la voiture. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>Il parle souvent ___ profiter pour aller voir ses amis.. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>Sa ___ est très sensible au froid. <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>Je suis ___ la cuisine. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>Il pensait ___ parler plus tard. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>Le docteur a examiné sa ___. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>J'ai laissé les clés ___ la poche de mon manteau. <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>Il a cassé une ___. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>
