<template>
  <h2 class="text-center"><i class="fas fa-calendar-check"></i> Confirmación de Asistencia</h2>
  <div class="confirmacion-widget container my-4">    
    <form @submit.prevent="enviarConfirmacion" class="needs-validation" novalidate>
      <div class="mb-3">
        <label for="nombre" class="form-label">Nombre Completo:</label>
        <input type="text" class="form-control" id="nombre" v-model="nombre" required>
        <div class="invalid-feedback">
          Por favor, introduce tu nombre.
        </div>
      </div>
      <div class="mb-3">
        <label for="telefono" class="form-label">Teléfono:</label>
        <input type="text" class="form-control" id="telefono" v-model="telefono" required>
        <div class="invalid-feedback">
          Por favor, introduce tu teléfono.
        </div>
      </div>
      <div class="mb-3">
        <label for="asistencia" class="form-label">Asistiré:</label>
        <select class="form-select" id="asistencia" v-model="asistencia" required>
          <option value="">Selecciona una opción</option>
          <option value="Sí">Sí</option>
          <option value="No">No</option>
        </select>
        <div class="invalid-feedback">
          Por favor, selecciona una opción.
        </div>
      </div>
      <button type="submit" class="btn btn-secondary">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'ConfirmacionWidget',
  data() {
    return {
      nombre: '',
      telefono: '',
      asistencia: ''
    };
  },
  methods: {
    enviarConfirmacion() {
      const scriptURL = "https://script.google.com/macros/s/AKfycbxyOQwr1PTSsFOKLO-B87TGAHnstKqAik_dVDtUN5qgOiYHRtNGsiXC_v_4yRYvYCM/exec"
      const formData = new URLSearchParams();
      formData.append("nombre", this.nombre);
      formData.append("telefono", this.telefono);
      formData.append("asistencia", this.asistencia);

      fetch(scriptURL, {
        method: 'POST',
        body: formData,
      }).then(() => {
        alert('Confirmación enviada');
        this.nombre = '';
        this.telefono = '';
        this.asistencia = '';
      }).catch(error => {
        console.error('Error al enviar la confirmación:', error);
      });
    }
  }
};
</script>

<style scoped>
.confirmacion-widget {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
</style>
