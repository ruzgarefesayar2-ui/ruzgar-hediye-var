# ruzgar-hediye-var <!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <title>Rüzgar tarafından hediye</title>
  <style>
    html, body {
      margin: 0; padding: 0; height: 100%; width: 100%;
      overflow: hidden;
      background: black;
      display: flex; justify-content: center; align-items: center;
      color: white;
      font-family: Arial, sans-serif;
      user-select: none;
    }
    #gift-link {
      font-size: 32px;
      cursor: pointer;
      text-align: center;
      user-select: none;
    }
    #jumpscare-video {
      display: none;
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      object-fit: cover;
      z-index: 9999;
    }
  </style>
</head>
<body>
  <div id="gift-link">Rüzgar tarafından hediye</div>
  <video id="jumpscare-video" src="https://media.vlipsy.com/vlips/Jy7sX1oQ/360p.mp4" autoplay playsinline></video>

<script>
  const giftLink = document.getElementById('gift-link');
  const video = document.getElementById('jumpscare-video');

  giftLink.addEventListener('click', () => {
    giftLink.style.display = 'none';
    video.style.display = 'block';
    video.volume = 1.0; // full ses
    video.play();
    if(video.requestFullscreen) {
      video.requestFullscreen();
    } else if(video.webkitRequestFullscreen) {
      video.webkitRequestFullscreen();
    } else if(video.msRequestFullscreen) {
      video.msRequestFullscreen();
    }
  });
</script>
</body>
</html>
