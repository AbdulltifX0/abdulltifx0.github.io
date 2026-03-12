
<html>
<head>
<title>Eid Greeting - HALA</title>

<style>
body {
  text-align: center;
  font-family: Arial;
}

#card {
  position: relative;
  display: inline-block;
  margin-top: 20px;
}

#card img {
  width: 600px;
}

#nameText {
  position: absolute;
  bottom: 120px;
  width: 100%;
  font-size: 28px;
  font-weight: bold;
  color: #333;
}
</style>
</head>

<body>

<h2>Eid Greeting </h2>

<input type="text" id="username" placeholder="Enter your name">
<button onclick="generateCard()">Generate</button>

<div id="card">

<a href="https://ibb.co/vCB2NrL4">
<img src="https://i.ibb.co/j957Cx3k/Hala-Eid-Greeting-04.jpg" alt="Hala-Eid-Greeting-04" border="0">
</a>

<div id="nameText"></div>

</div>

<script>
function generateCard() {
  var name = document.getElementById("username").value;
  document.getElementById("nameText").innerText = name;
}
</script>

</body>
</html>
