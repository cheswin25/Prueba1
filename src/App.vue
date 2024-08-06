2<template>
  <div id="app">
    <h1>Agenda de Contactos</h1>
    <ContactForm @add-contact="addContact" />
    <ContactList :contacts="contacts" @remove-contact="removeContact" />
  </div>
</template>

<script>
import ContactForm from './components/ContactForm.vue';
import ContactList from './components/Contactlista.vue';

export default {
  name: 'App',
  components: {
    ContactForm,
    ContactList
  },
  data() {
    return {
      contacts: []
    };
  },
  methods: {
    addContact(contact) {
      this.contacts.push(contact);
    },
    removeContact(index) {
      this.contacts.splice(index, 1);
    }
  }
}
</script>

<style >

body{
  padding: 0;
  margin: 0;
  color: rgb(0, 0, 0);
  background-color: rgb(203, 102, 102);
}
</style>