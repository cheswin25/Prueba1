
<script>
export default {
  data() {
    return {
      name: '',
      number: ''
    }
  },
  methods: {
    addContact() {
      this.$emit('add-contact', {
        name: this.name,
        number: this.number
      });
      this.name = '';
      this.number = '';
    }
  }
}
</script>
<template>
    <div>
      <h2>Añadir Contacto</h2>
      <form @submit.prevent="addContact">
        <label for="name">Nombre:</label>
        <input v-model="name" id="name" required>
        
        <label for="number">Número:</label>
        <input v-model="number" id="number" required>
        
        <button type="submit">Añadir</button>
      </form>
    </div>
  </template>
  