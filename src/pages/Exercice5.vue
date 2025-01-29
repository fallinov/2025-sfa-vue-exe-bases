<template>
  <v-container max-width="700">
    <!-- Donnée de l'exercice -->
    <exercice5-donnee />
    <!-- Zone de travail pour l'exercice -->
    <v-divider class="my-4" />
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Saisie surveillée</v-card-title>

        <v-card-text>
          <v-alert type="success" class="mb-2">
            Vous avez mentionné "Pokémon" !
          </v-alert>

          <v-text-field
            v-model="userInput"
            label="Tapez quelque chose"
            placeholder="Essayez d'écrire Pokémon"
            outlined
          />

          <v-card-subtitle>
            Nombre de caractères :
            *** CARACTÈRES SAISIS ***
          </v-card-subtitle>
        </v-card-text>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
// Importation du composant contenant la donnée de l'exerciced
import Exercice5Donnee from "@/components/donnees/Exercice5Donnee.vue";
// Importation de la fonction réactive ref
import { ref } from 'vue';

// Variable réactive pour la saisie utilisateur
const userInput = ref('');

// Longueur maximale autorisée
const MAX_LENGTH = 20;

// Variable réactive pour indiquer si "Pokémon" est présent
const containsPokemon = ref(false);
</script>
