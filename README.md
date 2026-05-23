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
      min-height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      overflow:hidden;

      /* IIT Tirupati Style Background */
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
      color:#ffffff;
      height:35px;
      font-weight:500;
    }

    .about{
      font-size:17px;
      line-height:1.9;
      color:#f1f1f1;
      margin-bottom:30px;
    }

    .buttons{
      display:flex;
      justify-content:center;
      gap:15px;
      flex-wrap:wrap;
      margin-bottom:25px;
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

    .social-icons{
      margin-top:10px;
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
      color:rgba(255,255,255,0.35);
      font-size:13px;
      letter-spacing:2px;
    }

    @media(max-width:768px){

      .container{
        padding:30px 20px;
      }

      h1{
        font-size:34px;
      }

      .typing{
        font-size:18px;
      }

      .about{
        font-size:15px;
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

    <!-- Replace this later with your own image -->
    <img src="https://i.pravatar.cc/300" alt="Ashok Kumar" class="profile-img">

    <h1>Ashok Kumar</h1>

    <div class="typing" id="typing-text"></div>

    <div class="about">

      Hello! I'm <strong>Ashok Kumar</strong>, currently pursuing
      <strong>M.Tech in Thermal Engineering at IIT Tirupati</strong> and
      working as a <strong>Proposal Engineer at Thermal Systems Pvt. Ltd.</strong>

      <br><br>

      I graduated from <strong>IIT Tirupati</strong> and have a strong passion
      for thermal engineering, industrial systems, innovation, and technology.
      I enjoy solving real-world engineering problems, learning modern tools,
      and building impactful solutions.

    </div>

    <div class="buttons">

      <a href="#" class="btn btn-primary">
        Contact Me
      </a>

      <a href="#" class="btn btn-secondary">
        My Projects
      </a>

    </div>

    <!-- Social Media Icons -->
    <div class="social-icons">

      <a href="https://www.instagram.com/ashoknke10" target="_blank">
        <i class="fab fa-instagram"></i>
      </a>

      <a href="#" target="_blank">
        <i class="fab fa-linkedin"></i>
      </a>

      <a href="#" target="_blank">
        <i class="fab fa-github"></i>
      </a>

    </div>

  </div>

  <!-- Watermark -->
  <div class="watermark">
    IIT Tirupati • Thermal Engineering
  </div>

  <script>

    const words = [
      "M.Tech @ IIT Tirupati",
      "Thermal Engineer",
      "Proposal Engineer",
      "Tech Enthusiast",
      "Problem Solver"
    ];

    let i = 0;
    let timer;

    function typingEffect() {

      let word = words[i].split("");

      var loopTyping = function() {

        if(word.length > 0) {

          document.getElementById('typing-text').innerHTML += word.shift();

        } else {

          deletingEffect();
          return false;
        }

        timer = setTimeout(loopTyping, 120);

      };

      loopTyping();

    };

    function deletingEffect() {

      let word = words[i].split("");

      var loopDeleting = function() {

        if(word.length > 0) {

          word.pop();

          document.getElementById('typing-text').innerHTML = word.join("");

        } else {

          if(words.length > (i + 1)) {

            i++;

          } else {

            i = 0;
          }

          typingEffect();
          return false;
        }

        timer = setTimeout(loopDeleting, 70);

      };

      loopDeleting();

    };

    typingEffect();

  </script>

</body>
</html>
