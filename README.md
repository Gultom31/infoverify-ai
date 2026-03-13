<!DOCTYPE html>
<html>
<head>
<title>InfoVerify AI</title>

<style>
body{
font-family: Arial;
background:#eef2f7;
text-align:center;
padding:40px;
}

.container{
background:white;
padding:30px;
width:500px;
margin:auto;
border-radius:10px;
box-shadow:0 0 10px rgba(0,0,0,0.2);
}

textarea{
width:100%;
height:120px;
padding:10px;
}

button{
background:#2b7cff;
color:white;
border:none;
padding:10px 20px;
font-size:16px;
margin-top:10px;
border-radius:5px;
cursor:pointer;
}

.result{
margin-top:20px;
font-size:18px;
font-weight:bold;
}
</style>

</head>

<body>

<div class="container">

<h2>InfoVerify AI</h2>
<p>Aplikasi AI untuk mengecek informasi digital</p>

<textarea id="inputText" placeholder="Masukkan informasi yang ingin diperiksa"></textarea>

<br><br>

<button onclick="cekInformasi()">Analisis Informasi</button>

<div class="result" id="hasil"></div>

</div>

<script>

function cekInformasi(){

let text=document.getElementById("inputText").value.toLowerCase();

let kataHoax=["katanya","rumor","hoax","tidak jelas","belum pasti"];

let hasil="";

for(let i=0;i<kataHoax.length;i++){

if(text.includes(kataHoax[i])){

hasil="⚠️ Informasi mencurigakan. Disarankan untuk memverifikasi sumber.";

document.getElementById("hasil").style.color="red";

document.getElementById("hasil").innerHTML=hasil;

return;

}

}

hasil="✅ Informasi terlihat aman, namun tetap periksa sumber terpercaya.";

document.getElementById("hasil").style.color="green";

document.getElementById("hasil").innerHTML=hasil;

}

</script>

</body>
</html>
