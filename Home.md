<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Intro Video</title>
  <style>
    body { margin: 0; background: black; color: white; }
    #skipBtn {
      position: absolute;
      top: 20px;
      right: 20px;
      padding: 10px 20px;
      background: crimson;
      color: white;
      border: none;
      cursor: pointer;
      z-index: 2;
    }
    video {
      width: 100%;
      height: 100vh;
      object-fit: cover;
    }
  </style>
</head>
<body>
  <button id="skipBtn">Skip Intro</button>
  <video autoplay muted playsinline id="introVideo">
    <source src="SpinDaBaby.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <script>
    document.getElementById('skipBtn').onclick = () => {
      window.location.href = "home.html";
    };
    document.getElementById('introVideo').addEventListener('ended', () => {
      window.location.href = "home.html";
    });
  </script>
</body>
</html>
