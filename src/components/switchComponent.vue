<template>
  <div>
    <b-field>
      <b-switch v-model="localDarkMode" passive-type="is-dark" type="is-warning">
        {{ localDarkMode ? "Dark Mode" : "Light Mode" }}
      </b-switch>
    </b-field>
  </div>
</template>

<script>
export default {
  name: 'switchComponent',
  props: {
    value: Boolean // Utilisez une prop nommée value pour le mode sombre
  },
  computed: {
    localDarkMode: {
      get() {
        return !this.value; // Inverser la valeur pour afficher le texte opposé
      },
      set(newValue) {
        this.$emit('input', !newValue); // Inverser la valeur avant d'émettre l'événement
      }
    }
  }
}
</script>

<style scoped>
/* Styles spécifiques au composant */
</style>
