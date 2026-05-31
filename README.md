<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Surprise</title>

<style>
body{
    font-family: Arial, sans-serif;
    text-align:center;
    background:#ffe6f0;
    margin:0;
    padding:20px;
}

.page{
    display:none;
}

.active{
    display:block;
}

button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:10px;
    cursor:pointer;
}

input{
    padding:10px;
    font-size:18px;
}

h1{
    color:#ff1493;
}

video{
    width:90%;
    max-width:500px;
    border-radius:15px;
}
</style>
</head>

<body>

<!-- Page 1 -->
<div id="page1" class="page active">
    <h1>🎂 Birthday Surprise 🎂</h1>
    <p>Enter Today's Date</p>
    <input type="date" id="dateInput">
    <br><br>
    <button onclick="checkDate()">Submit</button>
</div>

<!-- Page 2 -->
<div id="page2" class="page">
    <h1>🎉 Happy Birthday! 🎉</h1>

    <p>
        Wishing you endless happiness, success,
        laughter and beautiful memories.
        May all your dreams come true and
        your special day be filled with joy. ❤️
    </p>

    <button onclick="showVideo()">Continue</button>
</div>

<!-- Page 3 -->
<div id="page3" class="page">
    <h1>❤️ A Special Video For You ❤️</h1>

    <video controls autoplay>
        <source src="https://www.image2url.com/r2/default/videos/1780252536312-2ee76d0e-4e32-4f57-aeb3-62013953f1c3.mp4" type="video/mp4">
    </video>
</div>

<script>

function checkDate(){

    const entered =
        document.getElementById("dateInput").value;

    const today = new Date()
        .toISOString()
        .split('T')[0];

    if(entered === today){

        document.getElementById("page1")
            .classList.remove("active");

        document.getElementById("page2")
            .classList.add("active");

    }else{

        alert("Wrong date! Try again.");
    }
}

function showVideo(){

    document.getElementById("page2")
        .classList.remove("active");

    document.getElementById("page3")
        .classList.add("active");
}
</script>

</body>
</html>