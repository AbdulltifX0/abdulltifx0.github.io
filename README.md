
<html>
<head>
  <title>HALA Eid Greeting </title>
  <script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
    }

    #card {
      position: relative;
      display: inline-block;
      margin-top: 20px;
    }

    #card img {
      width: 600px;
      display: block;
    }

    #nameText {
      position: absolute;
      bottom: 120px;
      width: 100%;
      font-size: 28px;
      font-weight: bold;
      color: #333;
      text-align: center;
    }
  </style>
</head>
<body>

  <h2>HALA Eid Greeting </h2>

  <input type="text" id="username" placeholder="Enter your name">
  <br><br>

  <button onclick="generateCard()">Generate</button>
  <button onclick="downloadCard()">Download</button>

  <br><br>

  <div id="card">
    <img
      id="cardImage"
      src="https://i.ibb.co/j957Cx3k/Hala-Eid-Greeting-04.jpg"
      alt="Hala Eid Greeting"
      crossorigin="anonymous"
    >
    <div id="nameText"></div>
  </div>

  <script>
    function generateCard() {
      const name = document.getElementById("username").value;
      document.getElementById("nameText").innerText = name;
    }

    function downloadCard() {
      const card = document.getElementById("card");
      const img = document.getElementById("cardImage");

      if (!img.complete) {
        alert("Image is still loading. Please wait a moment and try again.");
        return;
      }

      html2canvas(card, {
        useCORS: true,
        allowTaint: false,
        backgroundColor: null,
        scale: 2
      }).then(canvas => {
        const link = document.createElement("a");
        link.download = "hala-eid-greeting.png";
        link.href = canvas.toDataURL("image/png");
        link.click();
      }).catch(err => {
        console.error(err);
        alert("Download failed. The image host may be blocking canvas access.");
      });
    }
  </script>

</body>
</html>
