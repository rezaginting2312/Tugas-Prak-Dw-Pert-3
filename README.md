# Tugas-Prak-Dw-Pert-3
<!DOCTYPE html>
<html lang="en">


<head>
   <meta charset="UTF-8">
   <meta http-equiv="X-UA-Compatible" content="IE=edge">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>SMA CAHAYA MEDAN</title>
   <link rel="stylesheet" href="DemoPrak3.css">
   <link rel="icon" type="image/x-icon" href="assets/img/favicon.ico">
</head>


<body>
   <header>
       <div class="container">
           <img src="https://2.bp.blogspot.com/-SqlE7mF2uJQ/UfoxL8Ug0PI/AAAAAAAAADs/CVoM7GucA_o/s320/logo-smac01.gif"
           alt="Logo SMA CAHAYA MEDAN" class="logo">
           <h1>SMA CAHAYA MEDAN</h1>
           <nav>
               <ul>
                   <li><a href="#">Home</a></li>
                   <li><a href="#">Tentang Kami</a></li>
                   <li><a href="#">Fasilitas</a></li>
                   <li><a href="#">Kontak</a></li>
               </ul>
           </nav>
       </div>
   </header>


   <section class="hero">
       <div class="container">
           <h2>Selamat Datang di Website Resmi SMK Negeri 1 Contoh</h2>
           <p>Website ini merupakan portal resmi untuk memberikan informasi terkini mengenai kegiatan sekolah dan
               akademik.</p>
       </div>
   </section>


   <section class="content">
       <div class="container">
           <h3>Informasi Terkini</h3>
           <p style="color: #fff;">Kami selalu menyediakan informasi terbaru mengenai kegiatan sekolah, pengumuman akademik, dan berita
               lainnya.</p>
       </div>
   </section>


   <section class="content">
       <div class="container">
           <div class="item">
               <h4>Pengumuman 1</h4>
               <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros.</p>
           </div>
           <div class="item">
               <h4>Pengumuman 2</h4>
               <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>
           </div>
           <div class="item">
               <h4>Pengumuman 3</h4>
               <p>Donec sollicitudin molestie malesuada. Cras ultricies ligula sed magna dictum porta.</p>
           </div>
       </div>
   </section>


   <footer>
       <div class="container">
           <p>&copy; 2024 SMK Negeri 1 Contoh. All Rights Reserved.</p>
       </div>
   </footer>


   <script>
       // Script untuk menampilkan/menyembunyikan menu di mobile
       const hamburger = document.getElementById('hamburger');
       const navLinks = document.getElementById('nav-links');


       hamburger.addEventListener('click', () => {
           // Toggle class 'active' untuk menampilkan atau menyembunyikan menu
           navLinks.classList.toggle('active');
           // Toggle ikon hamburger dan X
           hamburger.classList.toggle('open');
       });


       // (Opsional) Klik di luar area menu untuk menutupnya
       document.addEventListener('click', function(event) {
           const isClickInsideNav = hamburger.contains(event.target) || navLinks.contains(event.target);
           if (!isClickInsideNav) {
               navLinks.classList.remove('active');
               hamburger.classList.remove('open');  // Kembalikan ikon ke hamburger jika menu ditutup
           }
       });
   </script>
</body>


</html>


/* Import Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Open+Sans:wght@400;600&display=swap');


/* Reset CSS */
* {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
}


/* Body Style */
body {
   font-family: 'Open Sans', sans-serif;
   color: #333;
   background-image: url("https://fastly.4sqi.net/img/general/600x600/56079050_U2Yim_N96oHeRAcn7J0lIof1Kpsm06026UZL4Ij3P5c.jpg");
   background-size: cover;
   line-height: 1.6;
}


/* Container */
.container {
   width: 90%;
   max-width: 1200px;
   margin: 0 auto;
}


.container p{
   color: #fff;
}


/* Logo */
.logo {
   width: 100px; /* Sesuaikan ukuran logo */
   height: auto;
   float: left; /* Posisi logo di kiri */
   margin-right: 20px; /* Ruang antara logo dan teks */
}


/* Header */
header {
   background-color: #2C3E50;
   color: #fff;
   padding: 20px 0;
   text-align: center;
}


header h1 {
   font-family: 'Roboto', sans-serif;
   font-size: 36px;
}


/* Style umum */
nav {
   display: flex;
   justify-content: center;
   align-items: center;
}


nav ul {
   list-style: none;
   margin-top: 10px;
   padding: 0;
   display: flex;
   text-transform: uppercase;
   color: grey;
}


nav ul li {
   display: inline;
   margin-right: 20px;
   padding: 0 .5em .25em;
   cursor: pointer;
   position: relative;
   overflow: hidden;
   transition: .3s;
}


nav ul li a {
   color: #ecf0f1;
   text-decoration: none;
   font-weight: bold;
}


nav ul li a:hover {
   color: #3498db;
}


nav ul li:hover {
   color: #fff;
}


nav ul li:before {
   content: "";
   position: absolute;
   inset: calc(100% - 3px) 0 0 0;
   background: #ce4f20;
   scale: 0 1;
   transition: .3s, translate 0s .3s;
}


nav ul:hover li:before {
   scale: 1;
}


nav ul li:hover:before {
   translate: 0;
   transition: .3s;
}


nav ul:hover li:has(~ li:hover):before {
   translate: 100% 0;
   transition: .2s .2s, scale 0s .4s;
}


nav ul:hover li:hover~li:before {
   translate: -100% 0;
   transition: .2s .2s, scale 0s .4s;
}


/* Hero Section */
.hero {
   background-color: #3498db;
   color: #fff;
   padding: 50px 0;
   text-align: center;
}


.hero h2 {
   font-family: 'Roboto', sans-serif;
   font-size: 28px;
}


.hero p {
   font-size: 18px;
}


/* Content Section */
.content {
   padding: 50px 0;
   text-align: center;
}


.content h3 {
   font-family: 'Roboto', sans-serif;
   font-size: 24px;
   color: #2C3E50;
}


.content p {
   font-size: 16px;
   margin-top: 10px;
   color: #7f8c8d;
}


/* Footer */
footer {
   background-color: #2C3E50;
   color: #fff;
   text-align: center;
   padding: 20px 0;
}


footer p {
   margin: 0;
}


/* Responsive Design */
@media (max-width: 768px) {
   header h1 {
       font-size: 28px;
   }


   .hero h2 {
       font-size: 24px;
   }


   .content h3 {
       font-size: 20px;
   }


   nav ul li {
       display: block;
       margin: 10px 0;
   }
}


/* Content Grid Layout */
.content .container {
   display: grid;
   grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
   gap: 20px;
}


.content .item {
   background-color: #ecf0f1;
   padding: 20px;
   border-radius: 5px;
   text-align: left;
}


.content .item h4 {
   font-size: 20px;
   color: #2C3E50;
}


.content .item p {
   font-size: 14px;
   color: #7f8c8d;
}
