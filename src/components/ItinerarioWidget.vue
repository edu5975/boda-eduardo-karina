<template>
  <div class="itinerario-widget">
    <h2><i class="fas fa-calendar-alt"></i> Itinerario</h2>
    <div class="itinerario-list">
      <div v-for="(evento, index) in eventos" :key="index" class="itinerario-item">
        <div class="itinerario-time"><i class="fas fa-clock"></i> {{ evento.hora }}</div>
        <div class="itinerario-evento"><i :class="evento.icono"></i> {{ evento.descripcion }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItinerarioWidget',
  data() {
    return {
      eventos: [
        { hora: '10:00 AM', descripcion: 'Ceremonia en el Templo', icono:'fas fa-church'},
        { hora: '12:00 PM', descripcion: 'Recepción en el Salón', icono:'fas fa-glass-cheers' },
        { hora: '2:00 PM', descripcion: 'Almuerzo', icono:'fas fa-utensils'},
        { hora: '4:00 PM', descripcion: 'Sesión de Fotos', icono:'fas fa-camera'}
      ]
    };
  }
};
</script>

<style scoped>
.itinerario-widget {
  text-align: center;
  margin: 0 auto;
  margin-bottom: 20px;
  max-width: 80%;
}

.itinerario-list {
  margin-top: 20px;
}

.itinerario-item {
  background-color: #f8f9fa;
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: space-between; /* Alinea los elementos alrededor */
  align-items: center;
}

.itinerario-time {
  width: 35%; /* Ancho del 35% para la hora */
  font-size: 18px;
  font-weight: bold;
}

.itinerario-evento {
  width: 65%; /* Ancho del 65% para la descripción */
  font-size: 16px;
  display: flex;
  align-items: center;
}

.itinerario-evento i {
  margin-right: 5px;
}
</style>
