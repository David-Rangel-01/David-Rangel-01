## 「 David Rangel 」

<hr>
 <div align="justify">👋 Olá, me chamo David! Sou profissional de Segurança da Informação e com especialização em Desenvolvimento de Sistemas. Ao longo da minha jornada, aprofundei meus conhecimentos em programação, TI, Ethical Hacking, software e hardware. Tenho experiência sólida em sistemas Linux e Windows, além de um amplo domínio em linguagens de programação, segurança cibernética e desenvolvimento. Sempre em busca de novos desafios e aprendizados! </div>

<div style="display: inline_block"><br>
  <img align="center" alt="David-PyCharm" height="30" width="40" src="https://github.com/tandpfun/skill-icons/raw/main/icons/PyCharm-Dark.svg">
  <img align="center" alt="David-Vim" height="30" width="40" src="https://raw.githubusercontent.com/tandpfun/skill-icons/65dea6c4eaca7da319e552c09f4cf5a9a8dab2c8/icons/VIM-Dark.svg">
  <img align="center" alt="David-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="David-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="David-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
  <img align="center" alt="David-Css3" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg">

 <br>
  <img align="center" alt="David-Kali" height="30" width="40" src="https://github.com/tandpfun/skill-icons/raw/main/icons/Kali-Dark.svg">
  <img align="center" alt="David-Html" height="30" width="40" src="https://github.com/tandpfun/skill-icons/blob/main/icons/HTML.svg">
  <img align="center" alt="David-Arch" height="30" width="40" src="https://github.com/tandpfun/skill-icons/raw/main/icons/Arch-Dark.svg">
  <img align="center" alt="David-Neovim" heght="25" width="35" src="https://github.com/tandpfun/skill-icons/raw/main/icons/NeoVim-Dark.svg">
  <img align="center" alt="David-Cloud" height="30" width="40" src="https://github.com/tandpfun/skill-icons/raw/main/icons/GCP-Dark.svg">
  <img align="center" alt="David-Azure" height="30" width="40" src="https://github.com/tandpfun/skill-icons/raw/main/icons/Azure-Dark.svg">
  <img align="center" alt="David-Linux" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg">
  
</div>

##

<div> 
  <a href="https://www.linkedin.com/in/davidrrsoares/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

<img align="right" alt="David-GIF" height="210" src="https://i.pinimg.com/originals/c4/37/12/c43712af49b76ffbf268dd254800624d.gif">
 
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=David-Rangel-01&show_icons=true&theme=transparent)

<!doctype html>
<html>
<head>
  <meta charset="utf-8"/>
  <title>Snake</title>
  <style>
    html,body{height:100%;margin:0;display:flex;align-items:center;justify-content:center;background:#111;color:#eee;font-family:monospace}
    canvas{background:#000;border:6px solid #222}
    .info{position:fixed;top:10px;left:10px}
  </style>
</head>
<body>
  <div class="info">Use setas/WASD — Score: <span id="score">0</span></div>
  <canvas id="c" width="400" height="400"></canvas>
<script>
const canvas=document.getElementById('c'),ctx=canvas.getContext('2d');
const scale=20,cols=canvas.width/scale,rows=canvas.height/scale;
let snake=[{x:9,y:9}],dir={x:0,y:0},food=randomPos(),score=0;
document.getElementById('score').innerText=score;
document.addEventListener('keydown',e=>{
  const k=e.key;
  if(k==='ArrowUp'||k==='w') dir={x:0,y:-1};
  if(k==='ArrowDown'||k==='s') dir={x:0,y:1};
  if(k==='ArrowLeft'||k==='a') dir={x:-1,y:0};
  if(k==='ArrowRight'||k==='d') dir={x:1,y:0};
});
function randomPos(){return {x:Math.floor(Math.random()*cols), y:Math.floor(Math.random()*rows)}}
function loop(){
  const head={x:snake[0].x+dir.x, y:snake[0].y+dir.y};
  // borda wrap
  head.x=(head.x+cols)%cols; head.y=(head.y+rows)%rows;
  // colisão com corpo?
  if(snake.some(s=>s.x===head.x && s.y===head.y)){ alert('Game over! Score: '+score); reset(); return; }
  snake.unshift(head);
  if(head.x===food.x && head.y===food.y){
    score++; document.getElementById('score').innerText=score;
    food=randomPos();
  } else snake.pop();
  draw();
}
function reset(){ snake=[{x:9,y:9}]; dir={x:0,y:0}; food=randomPos(); score=0; document.getElementById('score').innerText=score; }
function draw(){
  ctx.fillStyle='#000'; ctx.fillRect(0,0,canvas.width,canvas.height);
  // food
  ctx.fillStyle='#e44'; ctx.fillRect(food.x*scale, food.y*scale, scale, scale);
  // snake
  ctx.fillStyle='#6f6'; snake.forEach((s,i)=> ctx.fillRect(s.x*scale+1, s.y*scale+1, scale-2, scale-2));
}
setInterval(loop,100);
</script>
</body>
</html>

  
</div>
