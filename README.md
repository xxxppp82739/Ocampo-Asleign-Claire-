<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Royal Page</title>

<style>
body {
  margin: 0;
  padding: 0;
  background: #3b0a0a;
  color: #c9a24a;
  font-family: "Times New Roman", Times, serif;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Sections */
.page {
  display: none;
  text-align: center;
  max-width: 700px;
}

.active {
  display: block;
}

/* Input */
input {
  background: transparent;
  border: 1px solid #c9a24a;
  color: #c9a24a;
  padding: 10px;
  font-family: "Times New Roman", Times, serif;
  text-align: center;
  margin-top: 15px;
}

/* Navigation */
nav {
  margin-bottom: 30px;
}

nav a {
  color: #c9a24a;
  text-decoration: none;
  margin: 0 15px;
  font-size: 18px;
  border-bottom: 1px solid transparent;
  cursor: pointer;
}

nav a:hover {
  border-bottom: 1px solid #c9a24a;
}

/* Title */
h1 {
  font-size: 48px;
  margin-bottom: 10px;
  letter-spacing: 2px;
}

/* Text */
p {
  font-size: 18px;
  line-height: 1.6;
}

/* Button */
.btn {
  display: inline-block;
  margin-top: 30px;
  padding: 10px 25px;
  border: 1px solid #c9a24a;
  color: #c9a24a;
  text-decoration: none;
  font-size: 16px;
  background: transparent;
  cursor: pointer;
}

.btn:hover {
  background: #c9a24a;
  color: #3b0a0a;
}
</style>
</head>

<body>

<!-- GATE -->
<div id="gate" class="page active">
  <h1>Who are you?</h1>
  <p>Very important</p>

  <input id="codeInput" type="text" placeholder="Enter here">
  <div class="btn" onclick="checkCode()">Continue</div>

  <p id="response" style="margin-top:20px;"></p>
  <div id="continueBtn" class="btn" style="display:none;" onclick="showPage('home')">
    Continue
  </div>
</div>

<!-- HOME -->
<div id="home" class="page">
  <nav>
    <a onclick="showPage('home')">Home</a>
    <a onclick="showPage('about')">About</a>
    <a onclick="showPage('message')">Message</a>
  </nav>

  <h1>Welcome</h1>
  <p>An elegant space, simple and refined.</p>
</div>

<!-- ABOUT -->
<div id="about" class="page">
  <nav>
    <a onclick="showPage('home')">Home</a>
    <a onclick="showPage('about')">About</a>
    <a onclick="showPage('message')">Message</a>
  </nav>

  <h1>About</h1>
  <p>
    HELLO, thank you for trusting this website, heheh don't worry there's no viruses here, 
    cause I made this website just for you lol
  </p>
</div>

<!-- MESSAGE -->
<div id="message" class="page">
  <nav>
    <a onclick="showPage('home')">Home</a>
    <a onclick="showPage('about')">About</a>
    <a onclick="showPage('message')">Message</a>
  </nav>

  <h1>For Asleign</h1>

  <p>
    This is probably the best that I can do to make you feel appreciated, 
    you are someone really REALLY REALLY special to me, 
    well not to mean it on a weird way, but still pretty special ig?
  </p>

  <div class="btn" onclick="showPage('next')">Next Page</div>
</div>

<!-- NEXT -->
<div id="next" class="page">
  <h1>For Asleign</h1>

  <p>
    I'm really afraid to lose you, I hope these little notes could make you happy 
    and brighten your day a bit.
  </p>

  <p>
    Sincerely — Michael
  </p>

  <div class="btn" onclick="showPage('message')">Back</div>
</div>

<script>
const validCodes = [
  "asleign",
  "asleign claire b. ocampo",
  "asleign ocampo",
  "claire",
  "claire ocampo"
];

function checkCode() {
  let input = document.getElementById("codeInput").value.toLowerCase().trim();
  let response = document.getElementById("response");
  let continueBtn = document.getElementById("continueBtn");

  if (validCodes.includes(input)) {
    response.textContent = "WHOAH ASLEIGN IT'S YOU, LOOK I MADE SOMETHING JUST FOR YOU!";
    continueBtn.style.display = "inline-block";
  } else {
    response.textContent = "EH YOU'RE NOT THE ONE I MADE THIS FOR! GET OUT!";
    continueBtn.style.display = "none";
  }
}

function showPage(pageId) {
  const pages = document.querySelectorAll('.page');
  pages.forEach(p => p.classList.remove('active'));
  document.getElementById(pageId).classList.add('active');
}
</script>

</body>
</html># Ocampo-Asleign-Claire-
