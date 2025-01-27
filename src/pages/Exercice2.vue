<template>
  <v-container>
    <v-card class="mx-auto" max-width="400">
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle
        :style="{ color: isHighlighted ? 'blue' : 'black' }"
      >
        {{ description }}
      </v-card-subtitle>
      <v-card-actions>
        <v-btn color="primary" @click="toggleHighlight">
          {{ isHighlighted ? "Réinitialiser la couleur" : "Mettre en surbrillance" }}
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Exercice1",
  data() {
    return {
      title: "Bienvenue à l'exercice 1",
      description: "Cet exercice démontre les bases du rendu déclaratif avec Vue.js.",
      isHighlighted: false, // Gère la couleur du texte
    };
  },
  methods: {
    toggleHighlight() {
      this.isHighlighted = !this.isHighlighted; // Inverse l'état
    },
  },
};
</script>

<style scoped>
.v-card {
  margin-top: 20px;
}
</style>
