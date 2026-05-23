<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ashok Kumar | Personal Portfolio</title>

  <!-- Google Font -->
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

      /* Background Image */
      background:
      linear-gradient(rgba(0,0,0,0.55), rgba(0,0,0,0.55)),
      url('https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=1920&auto=format&fit=crop')
      no-repeat center center/cover;
    }

    .card{
      width:90%;
      max-width:550px;
      padding:40px;
      border-radius:25px;

      background:rgba(255,255,255,0.12);
      backdrop-filter:blur(12px);

      text-align:center;
      color:white;

      border:1px solid rgba(255,255,255,0.2);

      box-shadow:0 8px 32px rgba(0,0,0,0.35);

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
      margin-bottom:10px;
      color:#00ffe7;
    }

    .typing{
      font-size:20px;
      color:#ffffff;
      margin-bottom:20px;
      min-height:30px;
    }

    p{
      font-size:17px;
      line-height:1.7;
      color:#f1f1f1;
      margin-bottom:25px;
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
      transform:scale(1.05);
    }

    .btn-secondary{
      border:2px solid #00ffe7;
      color:white;
    }

    .btn-secondary:hover{
      background:#00ffe7;
      color:black;
      transform:scale(1.05);
    }

    @media(max-width:600px){

      .card{
        padding:30px 20px;
      }

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
    }

  </style>
</head>

<body>

  <div class="card">

    <!-- Change this image later -->
    <img src="https://i.pravatar.cc/300" alt="Profile Photo" class="profile-img">

    <h1>Ashok Kumar</h1>

    <div class="typing" id="typing-text"></div>

    <p>
      Welcome to my personal portfolio website.
      Passionate about technology, creativity, coding,
      and learning new things every day.
    </p>

    <div class="buttons">
      <a href="#" class="btn btn-primary">Contact Me</a>
      <a href="#" class="btn btn-secondary">My Projects</a>
    </div>

  </div>

  <script>
    const text = [
      "Web Developer",
      "Tech Enthusiast",
      "Creative Learner",        
      "Future Engineer"
    ];

    let count = 0;
    let index = 0;
    let currentText = "";
    let letter = "";

    (function type(){

      if(count === text.length){
        count = 0;
      }

      currentText = text[count];
      letter = currentText.slice(0, ++index);

      document.getElementById('typing-text').textContent = letter;

      if(letter.length === currentText.length){
        count++;
        index = 0;
        setTimeout(type, 1200);
      } else {
        setTimeout(type, 120);
      }

    })();
  </script>

</body>
</html>
