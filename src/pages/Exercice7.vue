<template>
  <v-container max-width="700">
    <!-- Données de l'exercice -->
    <exercice-objectifs number="7"/>
    <!-- Zone de travail pour l'exercice -->
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Cyle de vie d'un composant Vue.js</v-card-title>

        <v-card-text>
          {{ count }}
        </v-card-text>

        <v-card-actions>
          <v-btn color="primary">
            Activer le champ de texte
          </v-btn>
        </v-card-actions>
      </v-card>
      <v-card
        class="mx-auto my-6 pa-2"
        max-width="500"
      >
        <p>Nombre actuel : {{ count }}</p>
        <v-btn @click="increment">Incrémenter</v-btn>
      </v-card>

    </div>
  </v-container>
</template>

<script setup>
import ExerciceObjectifs from "@/components/ExerciceObjectifs.vue";
import {ref, onMounted, onUpdated, onUnmounted} from 'vue';

const count = ref(0);

const increment = () => {
  count.value++;
};

onMounted(() => {
  alert('Composant monté avec succès !');
});

onUpdated(() => {
  alert('Composant mis à jour !');
});

onUnmounted(() => {
  alert('Composant démonté !');
});
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
