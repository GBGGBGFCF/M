
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Mon assistant jardinier</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background-color: #f4f4f4; }
    h1 { color: #2e7d32; }
    input, button { padding: 10px; margin-top: 10px; width: 300px; }
    button { background-color: #2e7d32; color: white; border: none; cursor: pointer; }
    p { margin-top: 20px; font-size: 1.1em; }
  </style>
</head>
<body>
  <h1>Pose ta question</h1>
  <input type="text" id="question" placeholder="Ex : Comment arroser une haie ?">
  <br>
  <button onclick="repondre()">Envoyer</button>
  <p id="reponse"></p>

  <script>
    function repondre() {
      const question = document.getElementById("question").value.toLowerCase();
      let reponse = "Je ne connais pas encore la réponse à cette question.";

      if (question.includes("arroser une haie")) {
        reponse = "Il faut arroser régulièrement, surtout l’été, tôt le matin ou tard le soir.";
      } else if (question.includes("tailler une haie")) {
        reponse = "La taille se fait généralement en fin d’hiver ou en été, selon la plante.";
      } else if (question.includes("quand planter")) {
        reponse = "La meilleure période pour planter est souvent l'automne ou le printemps, selon les plantes.";
      }

      document.getElementById("reponse").innerText = reponse;
    }
  </script>
</body>
</html>



