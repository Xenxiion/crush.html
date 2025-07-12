<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Crush Mo Ba Ako?</title>
  <style>
    body {
      background-color: #fff0f5;
      font-family: 'Comic Sans MS', cursive;
      text-align: center;
      margin-top: 100px;
    }

    h1 {
      color: #e91e63;
      font-size: 40px;
    }

    button {
      font-size: 30px;
      padding: 20px 30px;
      margin: 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    #ooBtn {
      background-color: #4caf50;
      color: white;
    }

    #hindiBtn {
      background-color: #f44336;
      color: white;
    }
  </style>
</head>
<body>
  <h1>Crush mo ba ako? </h1>
  <button id="ooBtn">Oo </button>
  <button id="hindiBtn">Hindi 😭</button>

  <script>
    const ooBtn = document.getElementById("ooBtn");
    const hindiBtn = document.getElementById("hindiBtn");

    let hindiClicks = 0;
    const hindiMessages = [
      " Are you sure ba kuya/ate?",
      " Ulitin mo nga...",
      "😡 Di nga? Parang hindi totoo!",
      "🤨 Hindi ka makakatakas!",
      "🚫 Ayyy mali. Wala nang atrasan!"
    ];

    hindiBtn.addEventListener("click", () => {
      if (hindiClicks < 4) {
        alert(hindiMessages[hindiClicks]);
        hindiClicks++;
      } else {
        alert(hindiMessages[4]);
        hindiBtn.disabled = true;
        hindiBtn.innerText = "Blocked ❌";
        hindiBtn.style.backgroundColor = "#999";
      }
    });

    ooBtn.addEventListener("click", () => {
      const hire = confirm("🎉 Congratulations! You have been selected as my jowa. Accept this job?");
      if (hire) {
        alert("Redirecting to orientation... 😘");
        window.location.href = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";
      } else {
        alert("You declined... but there's no escaping 💘");
        window.location.href = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";
      }
    });
  </script>
</body>
</html>
