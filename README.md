<!DOCTYPE html>
<html lang="kk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HTML Авто-Тексеру (Dark & Mobile)</title>
<style>
    body {
        font-family: Arial, sans-serif;
        padding: 20px;
        line-height: 1.6;
        background: #121212; /* Қара фон */
        color: #ffffff; /* Ақ мәтін */
        margin: 0;
    }

    h1, h2 {
        word-break: break-word;
    }

    textarea {
        width: 100%;
        height: 120px;
        font-family: monospace;
        background: #1e1e1e;
        color: #00ffea;
        border: 1px solid #333;
        padding: 10px;
        border-radius: 6px;
        box-sizing: border-box;
        font-size: 16px;
    }

    .task {
        background: #1c1c1c; /* Қою сұр блок */
        border: 2px solid #333;
        padding: 15px;
        margin-bottom: 25px;
        border-radius: 8px;
    }

    button {
        padding: 12px 25px;
        background: #0d6efd;
        color: white;
        border: none;
        border-radius: 6px;
        cursor: pointer;
        font-size: 16px;
        margin-top: 10px;
    }

    button:hover {
        background: #0b5ed7;
    }

    .result {
        font-weight: bold;
        margin-top: 10px;
        font-size: 18px;
        word-break: break-word;
    }

    .correct { color: #00ff6a; }
    .wrong { color: #ff4d4d; }

    /* Мобильдік бейімдеу */
    @media screen and (max-width: 600px) {
        body { padding: 10px; }
        textarea { height: 100px; font-size: 14px; }
        button { width: 100%; font-size: 15px; padding: 10px; }
    }
</style>
</head>
<body>

<h1>HTML тегтеріне арналған авто-тексеру жүйесі (Dark + Mobile)</h1>
<p>Оқушы кодты жазады → “Тексеру” → Дұрыс/Бұрыс шығады</p>
<hr>

<!-- ======= TASK 1 ======= -->
<div class="task">
<h2>1-тапсырма. Тақырып тегтері (h1–h6)</h2>
<p>Төмендегі мәтіндерді h тегтерімен дұрыс жазыңыз:</p>
<ul>
<li>HTML Сабақ → h1</li>
<li>1-тарау → h2</li>
<li>1.1 бөлім → h3</li>
<li>Қосымша ақпарат → h4</li>
</ul>
<textarea id="t1"></textarea>
<button onclick="check1()">Тексеру</button>
<div id="r1" class="result"></div>
</div>

<script>
function check1() {
    let a = document.getElementById("t1").value.replace(/\s+/g,"").toLowerCase();
    let correct =
    "<h1>htmlсабақ</h1><h2>1-тарау</h2><h3>1.1бөлім</h3><h4>қосымшаақпарат</h4>".replace(/\s+/g,"");
    document.getElementById("r1").innerHTML = (a === correct) ? "<span class='correct'>ДҰРЫС ✓</span>" : "<span class='wrong'>БҰРЫС ✗</span>";
}
</script>

<!-- ======= TASK 2 ======= -->
<div class="task">
<h2>2-тапсырма. Абзац (p)</h2>
<p>Мәтінді дұрыс &lt;p&gt; тегіне салыңыз:</p>
<textarea id="t2"></textarea>
<button onclick="check2()">Тексеру</button>
<div id="r2" class="result"></div>
</div>

<script>
function check2() {
    let a = document.getElementById("t2").value.replace(/\s+/g,"").toLowerCase();
    let correct =
    "<p>html—веб-беттердіқұруғаарналғанбелгілеутілі.олбраузергеақпараттыңқұрылымынкөрсетеді.</p>".replace(/\s+/g,"");
    document.getElementById("r2").innerHTML = (a === correct) ? "<span class='correct'>ДҰРЫС ✓</span>" : "<span class='wrong'>БҰРЫС ✗</span>";
}
</script>

<!-- ======= TASK 3 ======= -->
<div class="task">
<h2>3-тапсырма. br қолдану</h2>
<p>Екі сөйлемді p ішінде br арқылы бөлу керек:</p>
<textarea id="t3"></textarea>
<button onclick="check3()">Тексеру</button>
<div id="r3" class="result"></div>
</div>

<script>
function check3() {
    let a = document.getElementById("t3").value.replace(/\s+/g,"").toLowerCase();
    let correct =
    "<p>htmlтіліөтеманызды.<br>оныүйренувеб-әзірлеудіңнегізі.</p>".replace(/\s+/g,"");
    document.getElementById("r3").innerHTML = (a === correct) ? "<span class='correct'>ДҰРЫС ✓</span>" : "<span class='wrong'>БҰРЫС ✗</span>";
}
</script>

<!-- ======= TASK 4 ======= -->
<div class="task">
<h2>4-тапсырма. hr қолдану</h2>
<p>Екі абзац арасына көлденең сызық қойыңыз:</p>
<textarea id="t4"></textarea>
<button onclick="check4()">Тексеру</button>
<div id="r4" class="result"></div>
</div>

<script>
function check4() {
    let a = document.getElementById("t4").value.replace(/\s+/g,"").toLowerCase();
    let correct =
    "<p>абзац1:htmlтіліндээлементтертегарқылышазылады.</p><hr><p>абзац2:әртегтіңөзіндікқызметібар.</p>".replace(/\s+/g,"");
    document.getElementById("r4").innerHTML = (a === correct) ? "<span class='correct'>ДҰРЫС ✓</span>" : "<span class='wrong'>БҰРЫС ✗</span>";
}
</script>

<!-- ======= TASK 5 ======= -->
<div class="task">
<h2>5-тапсырма. Аралас тегтер</h2>
<p>Талап бойынша HTML құрыңыз:</p>
<textarea id="t5"></textarea>
<button onclick="check5()">Тексеру</button>
<div id="r5" class="result"></div>
</div>

<script>
function check5() {
    let a = document.getElementById("t5").value.replace(/\s+/g,"").toLowerCase();
    let correct =
    "<h1>htmlкіріспе</h1><p>бұлсабақтабізhtmlқұрылымынүйренеміз.<br>маңызды!</p><hr>".replace(/\s+/g,"");
    document.getElementById("r5").innerHTML = (a === correct) ? "<span class='correct'>ДҰРЫС ✓</span>" : "<span class='wrong'>БҰРЫС ✗</span>";
}
</script>

</body>
</html>
