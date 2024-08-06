<script>
export default {
  props: {
    contacts: Array
  },
  methods: {
    removeContact(index) {
      this.$emit('remove-contact', index);
    }
  }
}
</script>
<template>
    <div>
      <h2>Lista de Contactos</h2>
      <ul>
        <li v-for="(contact, index) in contacts" :key="index">
          {{ contact.name }} - {{ contact.number }}
          <button @click="removeContact(index)">Eliminar</button>
        </li>
      </ul>
    </div>
  </template>
  