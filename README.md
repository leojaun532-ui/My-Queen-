# My-Queen-
Te amo

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Galaxia para ti ❤️</title>
  <style>
    body { 
      margin:0; padding:0; background:#000; color:#fff; 
      font-family: 'Arial', sans-serif; text-align:center; 
      overflow:hidden; height:100vh; 
    }
    .stars { 
      position:fixed; top:0; left:0; width:100%; height:100%; 
      background: radial-gradient(circle, #ffffff 1px, transparent 1px); 
      background-size: 60px 60px; opacity:0.4; 
      animation: twinkle 8s infinite alternate; 
      pointer-events: none;
    }
    @keyframes twinkle { 0% {opacity:0.3;} 100% {opacity:0.8;} }
    
    h1 { margin-top: 15%; font-size: 2.8em; text-shadow: 0 0 30px #ff69b4; }
    p { font-size: 1.4em; margin: 15px 20px; line-height: 1.4; }
    .touch { 
      font-size: 1.2em; color:#ff99ff; margin-top: 40px; 
      animation: pulse 2s infinite; 
    }
    @keyframes pulse { 0%,100% {opacity:1;} 50% {opacity:0.6;} }
  </style>
</head>
<body>

  <div class="stars"></div>

  <h1>Mi galaxia solo para ti 🌌</h1>
  <p>Esta es nuestra canción...</p>
  <p><strong>Yo Te Voy A Amar - *NSYNC</strong></p>
  
  <div class="touch">
    ❤️ Toca cualquier parte de la pantalla y la música empezará sola ❤️
  </div>

  <!-- Música -->
  <audio id="musica" loop muted playsinline>
    <source src="https://files.catbox.moe/1v2l3k.mp3" type="audio/mpeg">
    Tu navegador no soporta audio.
  </audio>

  <script>
    const audio = document.getElementById('musica');
    
    // Al primer toque en la pantalla, quita el silencio y reproduce
    document.addEventListener('touchstart', function startMusic() {
      if (audio.muted) {
        audio.muted = false;
        audio.play().then(() => {
          console.log("¡Música reproduciéndose!");
        }).catch(err => {
          console.log("Todavía necesita un toque más");
        });
      }
    }, { once: true });

    // También funciona con clic (por si abre en computadora)
    document.addEventListener('click', function startMusic() {
      if (audio.muted) {
        audio.muted = false;
        audio.play();
      }
    }, { once: true });
  </script>

</body>
</html>
