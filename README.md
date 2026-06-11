<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Battle of Legends - Pendaftaran Esports</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    overflow:hidden;
    height:100vh;
    background:linear-gradient(#6ec6ff,#b3e5fc);
}

/* Langit */
.sky{
    position:absolute;
    width:100%;
    height:70%;
    background:linear-gradient(#6ec6ff,#b3e5fc);
}

/* Matahari */
.sun{
    position:absolute;
    top:50px;
    right:100px;
    width:100px;
    height:100px;
    background:gold;
    border-radius:50%;
    box-shadow:0 0 50px gold;
}

/* Laut */
.ocean{
    position:absolute;
    bottom:0;
    width:100%;
    height:40%;
    background:#00a2ff;
}

/* Pulau */
.island{
    position:absolute;
    bottom:140px;
    left:50%;
    transform:translateX(-50%);
    width:350px;
    height:120px;
    background:#d9a441;
    border-radius:50%;
}

/* Rumput */
.grass{
    position:absolute;
    top:-20px;
    left:20px;
    width:310px;
    height:60px;
    background:#2ecc71;
    border-radius:50%;
}

/* Pohon kelapa */
.trunk{
    position:absolute;
    left:210px;
    top:-130px;
    width:18px;
    height:130px;
    background:#8b5a2b;
    transform:rotate(15deg);
}

.leaf{
    position:absolute;
    width:90px;
    height:20px;
    background:#27ae60;
    border-radius:50px;
}

.l1{top:-140px;left:165px;transform:rotate(-20deg);}
.l2{top:-155px;left:175px;transform:rotate(20deg);}
.l3{top:-145px;left:205px;transform:rotate(70deg);}
.l4{top:-145px;left:135px;transform:rotate(-70deg);}

/* Panel Form */
.form-box{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:90%;
    max-width:450px;
    background:rgba(0,0,0,0.75);
    padding:25px;
    border-radius:20px;
    color:white;
    backdrop-filter:blur(10px);
}

.form-box h1{
    text-align:center;
    color:#00ffff;
    margin-bottom:10px;
}

.form-box p{
    text-align:center;
    margin-bottom:20px;
}

input{
    width:100%;
    padding:12px;
    margin-bottom:15px;
    border:none;
    border-radius:10px;
    background:#1e293b;
    color:white;
}

button{
    width:100%;
    padding:14px;
    border:none;
    border-radius:10px;
    background:#00ffff;
    color:black;
    font-weight:bold;
    cursor:pointer;
    font-size:16px;
}

button:hover{
    transform:scale(1.03);
}

.footer{
    text-align:center;
    margin-top:15px;
    color:#ccc;
}
</style>
</head>
<body>

<div class="sky">
    <div class="sun"></div>
</div>

<div class="ocean"></div>

<div class="island">
    <div class="grass"></div>

    <div class="trunk"></div>

    <div class="leaf l1"></div>
    <div class="leaf l2"></div>
    <div class="leaf l3"></div>
    <div class="leaf l4"></div>
</div>

<div class="form-box">

    <h1>⚔ BATTLE OF LEGENDS ⚔</h1>
    <p>Pendaftaran Player Esports</p>

    <form id="playerForm">

        <input
            type="text"
            id="nama"
            placeholder="Nama Player"
            required
        >

        <input
            type="text"
            id="idplayer"
            placeholder="ID Player Esports"
            required
        >

        <button type="submit">
            KIRIM PENDAFTARAN
        </button>

    </form>

    <div class="footer">
        Battle of Legends © 2026
    </div>

</div>

<script>
document.getElementById("playerForm")
.addEventListener("submit", function(e){

    e.preventDefault();

    const nama =
        document.getElementById("nama").value;

    const idplayer =
        document.getElementById("idplayer").value;

    const nomor =
        "6285166024686";

    const pesan =
`⚔ BATTLE OF LEGENDS ⚔

PENDAFTARAN PLAYER

Nama Player : ${nama}
ID Player : ${idplayer}

Data dikirim dari website Battle of Legends.`;

    const link =
        "https://wa.me/" +
        nomor +
        "?text=" +
        encodeURIComponent(pesan);

    window.open(link, "_blank");
});
</script>

</body>
</html>
