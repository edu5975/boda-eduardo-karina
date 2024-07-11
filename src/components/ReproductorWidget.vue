<template>
    <div class="reproductor text-center my-4">
      <h2><i class="fas fa-music"></i> Nuestra Canción</h2>
      <audio autoplay controls>
        <source src="../assets/cancion.mp3" type="audio/mpeg">
        Tu navegador no soporta el elemento de audio.
      </audio>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ReproductorWidget'
  };
  </script>
  