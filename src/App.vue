<template>
  <div id="app">
    <switchComponent v-model="darkMode" />
    <div v-if="darkMode" class="dark-mode">
      <!-- Contenu spécifique au mode sombre -->
      <h1>Mode Sombre Activé</h1>
      <!-- Autres éléments du mode sombre -->
    </div>
    <div v-else class="light-mode">
      <!-- Contenu spécifique au mode clair -->
      <h1>Mode Clair Activé</h1>
      <!-- Autres éléments du mode clair -->
    </div>
  </div>
</template>


<script>
import switchComponent from './components/switchComponent.vue';

export default {
  name: 'App',
  components: {
    switchComponent
  },
  data() {
    return {
      darkMode: true
    };
  }
}
</script>

<style>
#app {
  /* Styles communs */
}

.dark-mode {
  background-color: #333; /* Couleur de fond pour le mode sombre */
  color: #fff; /* Couleur du texte pour le mode sombre */
  height: 98vh;
}

.light-mode{
  background-color: aquamarine;
  color: black;
  height: 98vh;
}
</style>
