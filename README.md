<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ashok Kumar | Portfolio</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

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

      /* IIT / Modern Campus Style Background */
      background:
      linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.65)),
      url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?q=80&w=1920&auto=format&fit=crop')
      no-repeat center center/cover;
    }

    .container{
      width:90%;
      max-width:600px;
      padding:40px;
      border-radius:25px;

      background:rgba(255,255,255,0.12);
      backdrop-filter:blur(12px);

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
      width:170px;
      height:170px;
      border-radius:50%;
      object-fit:cover;

      border:5px solid #00ffe7;

      box-shadow:0 0 25px rgba(0,255,231,0.7);

      margin-bottom:20px;
    }

    h1{
      font-size:42px;
      color:#00ffe7;
      margin-bottom:10px;
    }

    .typing{
      font-size:22px;
      margin-bottom:20px;
      color:#ffffff;
      height:30px;
    }

    p{
      font-size:17px;
      line-height:1.8;
      margin-bottom:30px;
      color:#f1f1f1;
    }

    .buttons{
      display:flex;
      justify-content:center;
      gap:15px;
      flex-wrap:wrap;
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

    /* Watermark */
    .watermark{
      position:fixed;
      bottom:15px;
      right:20px;
      color:rgba(255,255,255,0.4);
      font-size:14px;
      letter-spacing:2px;
    }

    @media(max-width:600px){

      h1{
        font-size:32px;
      }

      .typing{
        font-size:18px;
      }

      p{
        font-size:15px;
      }

      .profile-img{
        width:130px;
        height:130px;
      }

      .container{
        padding:30px 20px;
      }
    }

  </style>
</head>

<body>

  <div class="container">

    <!-- Replace later with your image -->
    <img src="https://i.pravatar.cc/300" alt="Ashok Kumar" class="profile-img">

    <h1>Ashok Kumar</h1>

    <div class="typing" id="typing-text"></div>

    <p>
      Welcome to my personal portfolio website.
      Passionate about technology, innovation,
      coding, and building creative solutions.
    </p>

    <div class="buttons">
      <a href="#" class="btn btn-primary">Contact Me</a>
      <a href="#" class="btn btn-secondary">My Projects</a>
    </div>

  </div>

  <div class="watermark">
    Inspired by IIT Tirupati
  </div>

  <script>

    const words = [
      "Future Engineer",
      "Tech Enthusiast",
      "Web Developer",
      "Creative Learner"
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
        };

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
          };
          typingEffect();
          return false;
        };

        timer = setTimeout(loopDeleting, 70);

      };

      loopDeleting();

    };

    typingEffect();

  </script>

</body>
</html>
