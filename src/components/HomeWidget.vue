<template>
  <div class="home-widget container my-4">
    <h1>Nuestra Boda</h1>
    <h2>Eduardo Daniel Rico Gómez & Karina Itzel Rico Flores</h2>
    <p class="mensaje">Acompañanos a celebrar nuestro amor el día <strong><br>16 de Noviembre de 2025</strong></p>
    <h3>Padres</h3>
    <div class="row">
      <div class="col-12 col-md-6 my-2">
        <strong>Padres de Eduardo:</strong><br>Padre de Eduardo & Madre de Eduardo<br>
      </div>
      <div class="col-12 col-md-6 my-2">
        <strong>Padres de Karina:</strong><br>Padre de Karina & Madre de Karina
      </div>
    </div>
    <h3>Padrinos</h3>
    <div class="row">
      <div class="col-12 col-md-6 my-2">
        <strong>Padrino de Eduardo:</strong><br>Padrino de Eduardo & Madrina de Eduardo<br>
      </div>
      <div class="col-12 col-md-6 my-2">
        <strong>Padrino de Karina:</strong><br>Padrino de Karina & Madrina de Karina
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWidget',
};
</script>

<style scoped>
.home-widget {
  text-align: center;
}

.mensaje {
  font-size: 1.8em;
  padding: 30px;
}


</style>
