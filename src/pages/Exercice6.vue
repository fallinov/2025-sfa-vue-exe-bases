<template>
  <v-container max-width="700">
    <h1>Exercice 6</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>Découvrir et utiliser les hooks du <strong>cycle de vie</strong> dans Vue.js.</li>
        <li>
          Utiliser <code>onMounted</code> pour exécuter une action lorsque le composant est monté (par exemple, charger une donnée simulée).
        </li>
        <li>
          Utiliser <code>onUpdated</code> pour surveiller les changements d’une variable et afficher un message dans la console.
        </li>
        <li>
          Utiliser <code>onUnmounted</code> pour nettoyer une action (par exemple, annuler un intervalle).
        </li>
      </ul>
    </div>
    <v-divider class="my-4" />
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Cycle de vie de Vue.js</v-card-title>
        <v-card-text>
          <p>Compteur : <strong>{{ counter }}</strong></p>
          <v-btn color="primary" @click="incrementCounter">Incrémenter</v-btn>
        </v-card-text>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
import { ref, onMounted, onUpdated, onUnmounted } from 'vue';

// Variables réactives
const counter = ref(0);
let intervalId = null;

// Hook exécuté lorsque le composant est monté
onMounted(() => {
  console.log('Composant monté !');
  // Simule un intervalle qui met à jour le compteur automatiquement
  intervalId = setInterval(() => {
    counter.value++;
  }, 1000);
});

// Hook exécuté lorsque la variable "counter" est mise à jour
onUpdated(() => {
  console.log(`Le compteur a été mis à jour : ${counter.value}`);
});

// Hook exécuté lorsque le composant est démonté
onUnmounted(() => {
  console.log('Composant démonté !');
  // Nettoie l'intervalle pour éviter une fuite de mémoire
  clearInterval(intervalId);
});

// Fonction pour incrémenter manuellement le compteur
const incrementCounter = () => {
  counter.value++;
};
</script>

<style scoped>
.exe-objectifs {
  background-color: #f5f5f5;
  padding: 16px;
  border-radius: 8px;
}

.exe-zone {
  margin-top: 16px;
}
</style>
