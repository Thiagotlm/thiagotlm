<h3> Olá, eu sou Thiago Mauricio! Seja bem vindo(a) ao meu perfil GitHub! 👋🏻 </h3>  
<h4></h4>   
           
<h6> 💫 #desenvolvimentoweb, #computação, e #tecnologia </h6>

<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=44E3D3&height=120&section=header"/>

<div>
  <canvas id='canvas1'></canvas>
          const canvas = document.getElementById("canvas1");
const ctx = canvas.getContext("2d");
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let gradient = ctx.createLinearGradient(0, 0, canvas.width, canvas.height);
gradient.addColorStop(0.4, 'green');
gradient.addColorStop(0.6, 'blue');
gradient.addColorStop(0.8, 'red');

class Symbol {
  constructor(x, y, fontSize, canvasHeight) {
    this.characters =
      "✧☹︎☠︎☸︎☣︎☢︎☯︎♾♲✰❤︎✦⚛︎☭☮︎⚔︎⚒︎☄︎✵⚰︎☘︎⚘♨︎✞☺︎♘♞☆☃︎★☼☀︎☾◎☽☁︎™Ω℞№ℹ︎❂❁✡︎✣✶✺✷◦◉⦿☒✗☐☞◇☛⚙︎☑︎⌘✘✔︎✓⌔⌫⌁⌨︎⌗⌬⌖⌰⌭⌌⌏⌍⌱⌯⎔⍋⍒⍟⍊⎓⏍⍣⍦␗␄␡␢␛␀␥␦⑆⑇⑉⑈⏧⏦";
    this.x = x;
    this.y = y;
    this.fontSize = fontSize;
    this.text = "";
    this.canvasHeight = canvasHeight;
  }
  draw(context) {
    this.text = this.characters.charAt(
      Math.floor(Math.random() * this.characters.length)
    );
    context.fillText(this.text, this.x * this.fontSize, this.y * this.fontSize);
    if (this.y * this.fontSize > this.canvasHeight && Math.random() > 0.98) {
      this.y = 0;
    } else {
      this.y += 1;
    }
  }
}

class Effect {
  constructor(canvasWidth, canvasHeight) {
    this.canvasWidth = canvasWidth;
    this.canvasHeight = canvasHeight;
    this.fontSize = 25;
    this.columns = this.canvasWidth / this.fontSize;
    this.symbols = [];
    this.#initialize();
    console.log(this.symbols);
  }
  #initialize() {
    for (let i = 0; i < this.columns; i++) {
      this.symbols[i] = new Symbol(i, 0, this.fontSize, this.canvasHeight);
    }
  }
  resize(width, height) {
    this.canvasWidth = width;
    this.canvasHeigth = height;
    this.columns = this.canvasWidth/this.fontSize;
    this.symbols = [];
    this.#initialize();
  }
}

const effect = new Effect(canvas.width, canvas.height);
let lastTime = 0;
const fps = 30;
const nextFrame = 1000 / fps;
let timer = 0;

function animate(timeStamp) {
  const deltaTime = timeStamp - lastTime;
  lastTime = timeStamp;
  if (timer > nextFrame) {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.textAlign = "center";
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = gradient; //"#0aff0a";
    ctx.font = effect.fontSize + "px monospace";
    effect.symbols.forEach((symbol) => symbol.draw(ctx));
    timer = 0;
  } else {
    timer += deltaTime;
  }
  requestAnimationFrame(animate);
}

animate(0);

window.addEventListener("resize", function () {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
  effect.resize(canvas.width, canvas.height);
  gradient = ctx.createLinearGradient(0, 0, canvas.width, canvas.height);
  gradient.addColorStop(0.4, 'green');
  gradient.addColorStop(0.6, 'blue');
  gradient.addColorStop(0.8, 'red');
});
           
<div align="center">
  <a href="[https://github.com/Thiagotlm](https://github.com/Thiagotlm)"> 
  <img height="150em" src="https://github-readme-stats.vercel.app/api?username=Thiagotlm&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="150em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Thiagotlm&layout=compact&langs_count=16&theme=tokyonight"/>
</div>
</div>
<br>

<div  align="center"> 
  <div style="display: inline_block"><br>
    <img align="left" height="250" alt="coding-time" src="code.gif">
    <h1 align="center">Melhores Tecnologias <3</h1>
    <a href="https://pt.wikipedia.org/wiki/JavaScript" title="Sobre o JS"><img align="center" height="30" width="40" alt="js-icon"  src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
    <a href="https://pt.wikipedia.org/wiki/React_(JavaScript)" title="Sobre o React"><img align="center" height="30" width="40" alt="react-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
    <a href="https://pt.wikipedia.org/wiki/HTML5" title="Sobre o HTML5"><img align="center" height="30" width="40" alt="html-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
    <a href="https://pt.wikipedia.org/wiki/Cascading_Style_Sheets" title="Sobre o CSS"><img align="center" height="30" width="40" alt="css-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
      <a href="https://pt.wikipedia.org/wiki/Visual_Studio_Code" title="Sobre o VS Code"><img align="center" alt="Thiago-Vscode" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" />
   </div>
    
  
  <h1 align="center">Redes Sociais</h1>
    <a href = "mailto: Thiagom.aae@gmail.com">
      <img width="30" src="gmail.svg">
    </a>
    <a href = "https://www.linkedin.com/in/thiago-mauricio-570a68136/">
      <img width="25" src="linkedin.svg">
    </a>
       <a href = "https://www.instagram.com/thiagolmauricio/">
      <img width="25" src="instagram.png">
    </a>
</div>
  
![Snake animation](https://github.com/thiagotlm/thiagotlm/blob/output/github-contribution-grid-snake.svg)
  <div align="center">
 <i> A magical universe can be born from small ideas! ⭐️</i> <br> <br>
  <img src="https://github.com/AlianeAmaral/AlianeAmaral/blob/main/Fire-Pixel.gif" width="220">
            
 <img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=44E3D3&height=120&section=footer"/>
        
  
