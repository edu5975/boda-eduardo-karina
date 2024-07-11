<template>
    <div class="vestimenta-widget container my-4">
      <h2>Código de Vestimenta</h2>
      <div class="vestimenta-info">
        <img :src="vestimenta" alt="Formal">
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'VestimentaWidget',
    data: () => ({
      currentSlide: 0,
      vestimenta: require('@/assets/vestimenta.png')
    }),
  };
  </script>
  
  <style scoped>
  .vestimenta-widget {
    text-align: center;
    width: 80%;
  }

  img {
    width: 70%;
    max-width: 300px;
  }
  </style>
  