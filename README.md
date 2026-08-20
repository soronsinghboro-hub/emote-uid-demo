<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Emote UID Demo</title>
</head>
<body>

  <h1>🎮 Emote Sender</h1>

  <input id="uid" type="text" placeholder="Enter Player UID">

  <select id="emote">
    <option>Dance</option>
    <option>Laugh</option>
    <option>Wave</option>
    <option>Heart</option>
  </select>

  <button onclick="sendEmote()">SEND EMOTE</button>

  <p id="message"></p>

  <script>
    function sendEmote() {
      const uid = document.getElementById("uid").value.trim();
      const emote = document.getElementById("emote").value;

      if (!uid) {
        document.getElementById("message").textContent =
          "Pehle UID enter karo!";
        return;
      }

      document.getElementById("message").textContent =
        "Demo: " + emote + " selected for UID " + uid;
    }
  </script>

</body>
</html>
