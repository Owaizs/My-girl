<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Prettiest Girl I Love</title>
  <style>
    body {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f7f7f7;
      font-family: Arial, sans-serif;
    }
    h1 {
      color: #ff69b4;
      text-align: center;
    }
    a {
      margin-top: 20px;
      text-decoration: none;
      color: #fff;
      background-color: #ff69b4;
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 16px;
    }
    a:hover {
      background-color: #ff85c2;
    }
    .footer {
      position: absolute;
      bottom: 10px;
      font-size: 14px;
      color: #666;
    }
  </style>
</head>
<body>
  <h1>The Prettiest Girl I Love</h1>
  <a href="#" onclick="openCamera()">Click to Open Camera</a>

  <script>
    function openCamera() {
      navigator.mediaDevices.getUserMedia({ video: true })
        .then((stream) => {
          // Opens the camera if permissions are granted
          const video = document.createElement('video');
          video.srcObject = stream;
          video.play();
          document.body.innerHTML = ''; // Clear existing content
          document.body.appendChild(video);
        })
        .catch((error) => {
          alert('Camera access is blocked or not available!');
        });
    }
  </script>

  <!-- Footer added here -->
  <div class="footer">Designed by Owaiz</div>
</body>
</html>
