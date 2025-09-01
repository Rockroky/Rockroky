<!--
  Video di YouTube come background in loop,
  overlay nero leggero sopra,
  testo "Rockroky 👋" centrato in primo piano.
-->
<style>
.bg-container {
  position: relative;
  width: 100vw;
  height: 400px;
  overflow: hidden;
}
.bg-video {
  position: absolute;
  top: 50%;
  left: 50%;
  min-width: 100vw;
  min-height: 400px;
  width: auto;
  height: auto;
  transform: translate(-50%, -50%);
  z-index: 1;
  pointer-events: none;
  filter: blur(0.5px);
}
.bg-overlay {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0,0,0,0.55);
  z-index: 2;
}
.bg-text {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  z-index: 3;
  color: #fff;
  font-size: 4rem;
  font-family: Arial, sans-serif;
  font-weight: bold;
  text-shadow: 0 0 18px #ff0000, 0 0 4px #000;
  letter-spacing: 2px;
  text-align: center;
  user-select: none;
}
</style>

<div class="bg-container">
  <!-- YouTube embed con autoplay, loop, senza controls -->
  <iframe
    class="bg-video"
    src="https://www.youtube.com/embed/P_G_NCD-6rE?autoplay=1&mute=1&controls=0&showinfo=0&rel=0&loop=1&playlist=P_G_NCD-6rE&modestbranding=1"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
  ></iframe>
  <div class="bg-overlay"></div>
  <div class="bg-text">Rockroky 👋</div>
</div>
