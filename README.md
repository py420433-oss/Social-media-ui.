# Social-media-ui.
This website use to create like button 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aesthetic Social Media Website</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial;
}
body{
position:relative;
background:linear-gradient(135deg,#ffd6e7,#d6f0ff);
padding:20px;
}
.header{
text-align:center;
padding:30px;
}
.header img{
width:140px;
border-radius:50%;
border:5px solid white;
}
.header h1{
color:#ff4f81;
margin-top:15px;
}
.header, .card, nav, footer{
position:relative;
z-index:2;
}
.card{
background:white;
padding:20px;
border-radius:20px;
margin:20px auto;
max-width:500px;
box-shadow:0 5px 15px rgba(0,0,0,0.1);
}
textarea{
width:100%;
height:100px;
padding:15px;
border:none;
border-radius:15px;
background:#f2f2f2;
margin-top:15px;
}
.btn{
background:#ff4f81;
color:white;
border:none;
padding:12px 20px;
border-radius:30px;
margin-top:15px;
cursor:pointer;
}
.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(120px,1fr));
gap:15px;
margin-top:20px;
}
.gallery img{
width:100%;
border-radius:15px;
}
.profile{
text-align:center;
}
.profile img{
width:120px;
border-radius:50%;
}
.stats{
display:flex;
justify-content:space-around;
margin-top:20px;
}

footer{
text-align:center;
padding:20px;
color:#ff4f81;
font-weight:bold;
}
</style>
</head>
<body>
<div class="header">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png">
<h1>My social media  💖</h1>
<p>Cute Cartoon Social Media UI</p>
</div>

<div class="card">
<h2>Create Post</h2>
<textarea id="postInput" placeholder="What's on your mind?"></textarea>
<br>
<button class="btn" onclick="createPost()">Post</button>
</div>

<div id="posts"></div>

<div class="card">
<h2 style="text-align:center;">Cute Gallery ✨</h2>
<div class="card">
<h2 style="text-align:center;">Trending Posts 💖</h2>

<!-- Post 1 -->
<div class="card" style="margin-top:20px;">
<h3>ash  ✨</h3>

<img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png"
style="width:100%; border-radius:20px; margin-top:15px;">

<p style="margin:15px 0;">
Feeling cute today 💕
</p>

<button class="btn" onclick="likePost(this)">
❤️ Like <span>0</span>
</button>
</div>

<!-- Post 2 -->
<div class="card" style="margin-top:20px;">
<h3>Dream Girl 🌸</h3>

<img src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png"
style="width:100%; border-radius:20px; margin-top:15px;">

<p style="margin:15px 0;">
john ✨
</p>

<button class="btn" onclick="likePost(this)">
❤️ Like <span>0</span>
</button>
</div>

<!-- Post 3 -->
<div class="card" style="margin-top:20px;">
<h3>priyanka 💫</h3>

<img src="https://cdn-icons-png.flaticon.com/512/4140/4140051.png"
style="width:100%; border-radius:20px; margin-top:15px;">

<p style="margin:15px 0;">
Cute cartoon energy 🌈
</p>

<button class="btn" onclick="likePost(this)">
❤️ Like <span>0</span>
</button>
</div>

</div>

<div class="gallery">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140047.png">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140051.png">
</div>
</div>

<div class="card profile">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png">
<h2>Ash </h2>
<p>BCA Student | Frontend Developer</p>

<div class="stats">
<div>
<h3>120</h3>
<p>Posts</p>
</div>

<div>
<h3>5K</h3>
<p>Followers</p>
</div>

<div>
<h3>350</h3>
<p>Following</p>
</div>
</div>
</div>

<footer>
<nav style="position:fixed; bottom:20px; left:50%; transform:translateX(-50%); background:white; padding:15px 25px; border-radius:40px; display:flex; gap:20px; box-shadow:0 5px 15px rgba(0,0,0,0.2); z-index:1000;">

<button class="btn" onclick="showPage('homePage')">🏠 Home</button>
<button class="btn" onclick="showPage('profilePage')">👤 Profile</button>
<button class="btn" onclick="showPage('likePage')">Like</button>

</nav>

<div id="homePage" class="page">

<div class="card">
<h2>Create Post</h2>
<textarea id="postInput" placeholder="What's on your mind?"></textarea>
<br>
<button class="btn" onclick="createPost()">Post</button>
</div>

<div id="posts"></div>

<div class="card">
<h2 style="text-align:center;">Cute Gallery ✨</h2>

<div class="gallery">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140047.png">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140051.png">
</div>
</div>

</div>

<div id="profilePage" class="page" style="display:none;">

<div class="card profile">
<img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png">
<h2>Ash </h2>
<p>BCA Student | Frontend Developer</p>

<div class="stats">
<div>
<h3>120</h3>
<p>Posts</p>
</div>

<div>
<h3>5K</h3>
<p>Followers</p>
</div>

<div>
<h3>350</h3>
<p>Following</p>
</div>
</div>
</div>

</div>

<div id="likePage" class="page" style="display:none;">

<div class="card">
<h2 style="text-align:center;">Chat UI 💌</h2>
<div style="background:#f7f7f7; padding:15px; border-radius:15px; margin-top:20px;">
<p><b>Pikachu:</b> Hey 💖</p>
<p><b>Ash:</b> Hello ✨</p>
<p><b>Riya:</b> Cute 😍</p>
</div>
<input type="text" placeholder="Type message..." style="width:100%; padding:12px; margin-top:15px; border:none; border-radius:15px; background:#f2f2f2;">
<button class="btn">Send</button>
</div>

</div>

<div id="loginPage" class="page" style="display:none;">

<



<div class="card" id="chat">
<h2 style="text-align:center;">Chat UI 💌</h2>
<div style="background:#f7f7f7; padding:15px; border-radius:15px; margin-top:20px;">
<p><b>Riya:</b> Hey 💖</p>
<p><b>Ash:</b> Hello ✨</p>
<p><b>Pikachu:</b> Cuteb 😍</p>
</div>
<input type="text" placeholder="Type message..." style="width:100%; padding:12px; margin-top:15px; border:none; border-radius:15px; background:#f2f2f2;">
<button class="btn">Send</button>
</div>

<div class="card">
<h2 style="text-align:center;">Notifications 🔔</h2>
<ul style="margin-top:20px; line-height:2;">
<li>❤️ Someone liked your post</li>
</ul>
</div>

<button class="btn" onclick="toggleDarkMode()" style="position:fixed; bottom:20px; right:20px;">
🌙 Dark Mode
</button>

<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
</audio>

<script>
function showPage(pageId){

let pages=document.querySelectorAll('.page');

for(let i=0;i<pages.length;i++){
pages[i].style.display='none';
}

let activePage=document.getElementById(pageId);

if(activePage){
activePage.style.display='block';
window.scrollTo(0,0);
}
}

function toggleDarkMode(){
document.body.classList.toggle('dark');
}

for(let i=0;i<20;i++){
let heart=document.createElement('div');
heart.innerHTML='💖';
heart.style.position='fixed';
heart.style.left=Math.random()*100+'%';
heart.style.top=Math.random()*100+'%';
heart.style.fontSize='20px';
heart.style.opacity='0.3';
heart.style.zIndex='0';
heart.style.pointerEvents='none';
document.body.appendChild(heart);
}

for(let i=0;i<30;i++){
let star=document.createElement('div');
star.innerHTML='✨';
star.style.position='fixed';
star.style.left=Math.random()*100+'%';
star.style.top=Math.random()*100+'%';
star.style.fontSize='18px';
star.style.opacity='0.4';
star.style.zIndex='0';
star.style.pointerEvents='none';
document.body.appendChild(star);
}
</script>

<style>
.dark{
background:#111;
color:white;
}
.dark .card{
background:#222;
color:white;
}
</style>

<footer>
Made With 💖 By Priyanka
<section>

  <h1 style="text-align:center; color:#ff4f81; margin-bottom:40px;">
    Cute Gallery
  </h1>

  <div class="cards">

    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png" width="120">
      <h2>Dream boy</h2>
      <p>Beautiful cartoon aesthetic style.</p>
    </div>

    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png" width="120">
      <h2>Dream World</h2>
      <p>Soft pastel cartoon vibes.</p>
    </div>

    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/4140/4140051.png" width="120">
      <h2>Magic Theme</h2>
      <p>Cute modern animated design.</p>
    </div>

  </div>

</section>

<

  

</section>

<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
</audio>

<script>

for(let i=0;i<50;i++){
  let star=document.createElement('div');
  star.innerHTML='✨';
  star.style.position='fixed';
  star.style.left=Math.random()*100+'%';
  star.style.top=Math.random()*100+'%';
  star.style.fontSize='20px';
  document.body.appendChild(star);
}

</script>



`<footer>` 

```html
<section style="padding:70px 20px;">

<h1 style="text-align:center; color:#ff4f81; margin-bottom:40px;">
  Social Media UI
</h1>

<div class="card" style="max-width:500px; margin:auto;">

  <div style="display:flex; align-items:center; gap:15px; margin-bottom:20px;">
    <img src="https://cdn-icons-png.flaticon.com/512/4140/4140048.png"
    width="60" style="border-radius:50%;">

    <div>
      <h3>Priyanka Yadav</h3>
      <p>@cuteprofile</p>
    </div>
  </div>

  <textarea id="postText"
  placeholder="What's on your mind?"
  style="width:100%; height:100px; padding:15px; border-radius:20px; border:none; background:#f3f3f3;"></textarea>

  <button class="btn" onclick="createPost()">
    Create Post
  </button>

</div>

<div id="posts" style="margin-top:40px;"></div>

</section>

<section style="padding:70px 20px; text-align:center;">

<h1 style="color:#ff4f81; margin-bottom:40px;">
  Profile Page
</h1>

<div class="card" style="max-width:400px; margin:auto;">

  <img src="https://cdn-icons-png.flaticon.com/512/4140/4140047.png"
  width="140"
  style="border-radius:50%; margin-bottom:20px; border:5px solid #ff4f81;">

  <h2>Priyanka Yadav</h2>
  <p>BCA Student | Frontend Developer | Aesthetic Designer 💖</p>

  <div style="display:flex; justify-content:space-around; margin-top:25px;">
    <div>
      <h3>120</h3>
      <p>Posts</p>
    </div>

    <div>
      <h3>5K</h3>
      <p>Followers</p>
    </div>

    <div>
      <h3>350</h3>
      <p>Following</p>
    </div>
  </div>

</div>

</section>

<script>

function createPost(){

  let text=document.getElementById('postText').value;

  if(text===''){
    alert('Write something first');
    return;
  }

  let post=document.createElement('div');

  post.innerHTML=`

  <div class="card" style="max-width:500px; margin:20px auto;">

    <h3>Priyanka Yadav</h3>

    <p style="margin:20px 0;">${text}</p>

    <button class="btn" onclick="likePost(this)">❤️ Like <span>0</span></button>

    <br><br>

    <input type="text" placeholder="Write comment"
    style="padding:10px; width:70%; border-radius:20px; border:none; background:#f3f3f3;">

    <button class="btn">Comment</button>

  </div>

  `;

  document.getElementById('posts').prepend(post);

  document.getElementById('postText').value='';
}

function likePost(btn){

  let count=btn.querySelector('span');

  count.innerText=parseInt(count.innerText)+1;
}

</script>

</footer>

<script>
function createPost(){

let input=document.getElementById('postInput');

if(input.value===""){
alert('Please write something');
return;
}

let post=document.createElement('div');

post.className='card';

post.innerHTML=`
<h3>Priyanka Yadav</h3>
<p style="margin:15px 0;">${input.value}</p>
<button class="btn" onclick="likePost(this)">❤️ Like <span>0</span></button>
`;

document.getElementById('posts').prepend(post);

input.value='';
}

function likePost(btn){
let span=btn.querySelector('span');
span.innerText=parseInt(span.innerText)+1;
}
</script>

</body>
</html>
