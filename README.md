
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ashok Kumar | Personal Website</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;

      /* Background Image */
      background: url('background.jpg') no-repeat center center/cover;
    }

    .container {
      background: rgba(0, 0, 0, 0.6);
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      color: white;
      width: 90%;
      max-width: 500px;

      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
      backdrop-filter: blur(5px);
    }

    .profile-img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      border: 5px solid white;
      object-fit: cover;
      margin-bottom: 20px;
    }

    h1 {
      font-size: 38px;
      margin-bottom: 10px;
      color: #00ffd5;
    }

    p {
      font-size: 18px;
      line-height: 1.6;
      margin-bottom: 15px;
    }

    .btn {
      display: inline-block;
      padding: 12px 25px;
      background: #00ffd5;
      color: black;
      text-decoration: none;
      border-radius: 30px;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn:hover {
      background: white;
      transform: scale(1.05);
    }

    @media(max-width: 600px) {
      h1 {
        font-size: 30px;
      }

      p {
        font-size: 16px;
      }

      .profile-img {
        width: 120px;
        height: 120px;
      }
    }
  </style>
</head>

<body>

  <div class="container">

    <!-- Your Photo -->
    <img src="myphoto.jpg" alt="Ashok Kumar" class="profile-img">

    <h1>Hello, I'm Ashok Kumar</h1>

    <p>
      Welcome to my personal webpage!
    </p>

    <p>
      Passionate about technology, creativity, and learning new things.
    </p>

    <a href="#" class="btn">Contact Me</a>

  </div>

</body>
</html>
