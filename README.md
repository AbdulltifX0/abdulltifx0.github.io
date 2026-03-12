<!DOCTYPE html>
<html>
<head>
<title>HALA Eid Greeting Generator</title>

<script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>

<style>
body{
  text-align:center;
  font-family:Arial;
}

#card{
  position:relative;
  display:inline-block;
  margin-top:20px;
}

#card img{
  width:600px;
}

#nameText{
  position:absolute;
  bottom:120px;
  width:100%;
  font-size:28px;
  font-weight:bold;
  color:#333;
}
</style>
</head>

<body>

<h2>HALA Eid Greeting Generator</h2>

<input type="text" id="username" placeholder="Enter your name">
<br><br>

<button onclick="generateCard()">Generate</button>
<button onclick="downloadCard()">Download</button>

<br><br>

<div id="card">

<img src="https://i.ibb.co/j957Cx3k/Hala-Eid-Greeting-04.jpg">

<div id="nameText"></div>

</div>

<script>

function generateCard(){
var name=document.getElementById("username").value;
document.getElementById("nameText").innerText=name;
}

function downloadCard(){
html2canvas(document.querySelector("#card")).then(canvas=>{
var link=document.createElement("a");
link.download="hala-eid-greeting.png";
link.href=canvas.toDataURL();
link.click();
});
}

</script>

</body>
</html>
