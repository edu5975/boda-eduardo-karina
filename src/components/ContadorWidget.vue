<template>
  <div class="contador-widget text-center my-4">
    <h2><i class="fas fa-clock"></i> Cuenta Regresiva</h2>
    <div class="contador-container">
      <div class="contador-item">
        <div class="contador-value">{{ dias }}</div>
        <div class="contador-label">Días</div>
      </div>
      <div class="contador-item">
        <div class="contador-value">{{ horas }}</div>
        <div class="contador-label">Horas</div>
      </div>
      <div class="contador-item">
        <div class="contador-value">{{ minutos }}</div>
        <div class="contador-label">Minutos</div>
      </div>
      <div class="contador-item">
        <div class="contador-value">{{ segundos }}</div>
        <div class="contador-label">Segundos</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContadorWidget',
  data() {
    return {
      dias: '',
      horas: '',
      minutos: '',
      segundos: ''
    };
  },
  created() {
    this.actualizarTiempoRestante();
    setInterval(this.actualizarTiempoRestante, 1000);
  },
  methods: {
    actualizarTiempoRestante() {
      const eventoFecha = new Date('2025-11-16T16:00:00');
      const ahora = new Date();
      const diferencia = eventoFecha - ahora;

      this.dias = Math.floor(diferencia / (1000 * 60 * 60 * 24));
      this.horas = Math.floor((diferencia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      this.minutos = Math.floor((diferencia % (1000 * 60 * 60)) / (1000 * 60));
      this.segundos = Math.floor((diferencia % (1000 * 60)) / 1000);
    }
  }
};
</script>

<style scoped>
.contador-widget {
  padding: 10px;
}

.contador-container {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.contador-item {
  text-align: center;
  padding: 10px;
  border-radius: 8px;
  color: #fff;
  background-color: #333;
  width: 90px;
  height: 110px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contador-value {
  font-size: 2rem;
  font-weight: bold;
  animation: pulse 1s ease-in-out infinite alternate;
}

.contador-label {
  font-size: 1rem;
  text-transform: uppercase;
  opacity: 0.7;
}

</style>
