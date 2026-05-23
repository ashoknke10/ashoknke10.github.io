<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ashok Kumar | Portfolio</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome Icons -->
  <link rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
    }

    body{
      font-family:'Poppins',sans-serif;
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      overflow:hidden;

      /* Background Image */
      background:
      linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
      url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?q=80&w=1920&auto=format&fit=crop')
      no-repeat center center/cover;
    }

    .container{
      width:90%;
      max-width:700px;
      padding:40px;
      border-radius:25px;

      background:rgba(255,255,255,0.12);
      backdrop-filter:blur(14px);

      border:1px solid rgba(255,255,255,0.2);

      box-shadow:0 8px 32px rgba(0,0,0,0.4);

      text-align:center;
      color:white;

      animation:fadeIn 1.5s ease;
    }

    @keyframes fadeIn{
      from{
        opacity:0;
        transform:translateY(30px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    .profile-img{
      width:180px;
      height:180px;
      border-radius:50%;
      object-fit:cover;

      border:5px solid #00ffe7;
      box-shadow:0 0 30px rgba(0,255,231,0.7);

      margin-bottom:20px;
    }

    h1{
      font-size:45px;
      margin-bottom:10px;
      color:#00ffe7;
    }

    .typing{
      font-size:22px;
      margin-bottom:20px;
      height:35px;
      font-weight:500;
    }

    .about{
      font-size:16.5px;
      line-height:1.8;
      margin-bottom:30px;
      color:#f1f1f1;
    }

    .buttons{
      display:flex;
      justify-content:center;
      gap:15px;
      flex-wrap:wrap;
      margin-bottom:20px;
    }

    .btn{
      padding:12px 28px;
      border-radius:30px;
      text-decoration:none;
      font-weight:600;
      transition:0.3s;
    }

    .btn-primary{
      background:#00ffe7;
      color:black;
    }

    .btn-primary:hover{
      background:white;
      transform:scale(1.08);
    }

    .btn-secondary{
      border:2px solid #00ffe7;
      color:white;
    }

    .btn-secondary:hover{
      background:#00ffe7;
      color:black;
      transform:scale(1.08);
    }

    .social-icons a{
      color:white;
      font-size:24px;
      margin:0 12px;
      transition:0.3s;
    }

    .social-icons a:hover{
      color:#00ffe7;
      transform:scale(1.2);
    }

    .watermark{
      position:fixed;
      bottom:15px;
      right:20px;
      font-size:13px;
      color:rgba(255,255,255,0.4);
      letter-spacing:2px;
    }

    @media(max-width:768px){

      h1{
        font-size:32px;
      }

      .typing{
        font-size:18px;
      }

      .about{
        font-size:14.5px;
      }

      .profile-img{
        width:140px;
        height:140px;
      }
    }

  </style>
</head>

<body>

  <div class="container">

    <!-- Profile Image (replace later) -->
    <img src="https://i.pravatar.cc/300" class="profile-img" alt="Profile">

    <h1>Ashok Kumar</h1>

    <div class="typing" id="typing-text"></div>

    <div class="about">

      Hello! I'm <strong>Ashok Kumar</strong>, currently pursuing
      <strong>M.Tech in Thermal Engineering at IIT Tirupati</strong> and working as a
      <strong>Proposal Engineer at Thermal Systems Pvt. Ltd.</strong>

      <br><br>

      I graduated from <strong>IIT Tirupati</strong> and have strong interest in
      thermal systems, engineering design, industrial problem solving, and modern technologies.
      I enjoy learning, research, and building impactful engineering solutions.

    </div>

    <div class="buttons">

      <a href="#" class="btn btn-primary">Contact Me</a>
      <a href="#" class="btn btn-secondary">My Projects</a>

    </div>

    <!-- Social Links -->
    <div class="social-icons">

      <a href="https://www.instagram.com/ashoknke10" target="_blank">
        <i class="fab fa-instagram"></i>
      </a>

      <a href="https://www.linkedin.com/in/ashoknke10" target="_blank">
        <i class="fab fa-linkedin"></i>
      </a>

      <a href="#" target="_blank">
        <i class="fab fa-github"></i>
      </a>

    </div>

  </div>

  <div class="watermark">
    IIT Tirupati • Thermal Engineering
  </div>

  <script>

    const words = [
      "M.Tech @ IIT Tirupati",
      "Proposal Engineer",
      "Thermal Engineer",
      "Problem Solver",
      "Tech Enthusiast"
    ];

    let i = 0;

    function typingEffect() {

      let word = words[i].split("");
      let el = document.getElementById("typing-text");

      el.textContent = "";

      let interval = setInterval(() => {

        if(word.length > 0){
          el.textContent += word.shift();
        } else {
          clearInterval(interval);
          setTimeout(() => {
            i = (i + 1) % words.length;
            typingEffect();
          }, 1200);
        }

      }, 100);

    }

    typingEffect();

  </script>

</body>
</html>
