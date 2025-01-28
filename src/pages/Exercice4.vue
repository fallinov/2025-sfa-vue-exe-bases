<template>
  <v-container max-width="700">
    <h1>Exercice 4</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>
          Utiliser une <strong>propriété calculée</strong> pour afficher dynamiquement le nombre de caractères restants dans une limite définie.
        </li>
        <li>
          Utiliser une <strong>référence (ref)</strong> pour accéder à un élément du DOM et en modifier son focus.
        </li>
        <li>
          Afficher un message lorsque l'utilisateur atteint la limite maximale de caractères autorisés.
        </li>
      </ul>
    </div>
    <v-divider class="my-4" />
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Saisie avec limite de caractères</v-card-title>
        <v-card-text>
          <v-textarea
            v-model="userInput"
            outlined
            rows="3"
            ref="textareaRef"
            label="Tapez votre texte ici"
            :counter="maxLength"
          ></v-textarea>
          <v-alert v-if="remainingChars === 0" type="error" class="mt-4">
            Vous avez atteint la limite maximale de caractères !
          </v-alert>
          <v-card-subtitle>
            Caractères restants : <strong>{{ remainingChars }}</strong>
          </v-card-subtitle>
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" @click="focusTextarea">
            Mettre le focus dans la zone de texte
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
import { ref, computed } from 'vue';

// Variables réactives
const userInput = ref('');
const maxLength = 100;

// Propriété calculée pour déterminer le nombre de caractères restants
const remainingChars = computed(() => maxLength - userInput.value.length);

// Référence pour accéder à l'élément de la zone de texte
const textareaRef = ref(null);

// Fonction pour mettre le focus dans la zone de texte
const focusTextarea = () => {
  textareaRef.value.focus();
};
</script>
