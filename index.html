<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>YouTube Background Video</title>
  <style>
    /* Make the page fill the viewport */
    html,body{height:100%;margin:0;font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial}
    .bg-video-wrapper{position:fixed;inset:0;overflow:hidden;z-index:-1}
    /* Responsive iframe that covers the viewport */
    .bg-video-wrapper iframe{
      position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);
      width:177.77vh; /* 16:9 width relative to viewport height to ensure cover */
      height:100vh;min-width:100vw;min-height:56.25vw; /* ensure it always covers */
      pointer-events:none; /* allow clicks to pass through */
    }

    /* Content that sits on top of the video */
    .content{
      position:relative;z-index:10;display:flex;flex-direction:column;align-items:center;justify-content:center;height:100vh;color:white;text-align:center;padding:2rem;
      background:linear-gradient(180deg, rgba(0,0,0,0.15), rgba(0,0,0,0.45));
      box-sizing:border-box;
    }

    h1{font-size:clamp(1.6rem,4vw,3.2rem);margin:0 0 0.5rem}
    p{max-width:900px;margin:0 0 1rem;font-size:clamp(1rem,1.6vw,1.2rem);opacity:0.9}

    /* Small controls for user (mute/play) */
    .controls{display:flex;gap:0.6rem}
    .btn{background:rgba(255,255,255,0.12);border:1px solid rgba(255,255,255,0.18);color:white;padding:0.6rem 0.9rem;border-radius:10px;cursor:pointer}

    /* Make sure link styles visible */
    a{color:#fff;text-decoration:underline}
  </style>
</head>
<body>
  <!-- Background YouTube iframe -->
  <div class="bg-video-wrapper" aria-hidden="true">
    <iframe id="yt-player" src="https://www.youtube.com/embed/1ftGlk7neA8?autoplay=1&mute=0&controls=0&showinfo=0&rel=0&modestbranding=1&loop=1&playlist=1ftGlk7neA8&iv_load_policy=3" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
  </div>

  

  <script>
    // Simple postMessage control for the YouTube iframe
    // Note: Some browsers may restrict autoplay on mobile even when muted.
    const iframe = document.getElementById('yt-player');
    const muteBtn = document.getElementById('muteBtn');
    const playBtn = document.getElementById('playBtn');

    // Helper to send commands to player using the iframe API (postMessage)
    function postCommand(command, args) {
      iframe.contentWindow.postMessage(JSON.stringify(Object.assign({
        event: 'command',
        func: command,
      }, args || {})), '*');
    }

    // Wait a short time and then try to enable API control by inserting enablejsapi=1 if needed.
    // (We used embed URL without enablejsapi param — postMessage commands still work in many browsers.)

    let isMuted = true;
    let isPlaying = true;

    muteBtn.addEventListener('click', ()=>{
      if(isMuted){ postCommand('unMute'); muteBtn.textContent='Mute'; isMuted=false; }
      else { postCommand('unMute'); muteBtn.textContent='Unmute'; isMuted=true; }
    });

    playBtn.addEventListener('click', ()=>{
      if(isPlaying){ postCommand('pauseVideo'); playBtn.textContent='Play'; isPlaying=false; }
      else { postCommand('playVideo'); playBtn.textContent='Pause'; isPlaying=true; }
    });

    // Attempt to set initial state after load
    window.addEventListener('message', function onMessage(e){
      // ignore for now; placeholder in case YouTube sends events
    });

    // Accessibility: allow keyboard to toggle
    document.addEventListener('keydown', (e)=>{
      if(e.key===' '){ e.preventDefault(); playBtn.click(); }
      if(e.key==='m' || e.key==='M'){ muteBtn.click(); }
    });
  </script>
</body>
</html>
