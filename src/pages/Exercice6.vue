<template>
  <v-container max-width="700">
    <h1>Exercice 6</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>Apprendre à utiliser les <strong>watchers</strong> pour surveiller les changements d’une variable réactive.</li>
        <li>
          Surveiller la saisie utilisateur et afficher un message lorsque le texte contient le mot <strong>"Pokémon"</strong>.
        </li>
        <li>Afficher dynamiquement le nombre de caractères saisis.</li>
        <li>Utiliser un watcher pour réinitialiser automatiquement la saisie si elle dépasse une certaine longueur.</li>
      </ul>
    </div>
    <v-divider class="my-4" />
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Saisie surveillée</v-card-title>
        <v-card-text>
          <v-text-field
            v-model="userInput"
            label="Tapez quelque chose"
            placeholder="Essayez d'écrire Pokémon"
            outlined
          ></v-text-field>
          <v-card-subtitle>Nombre de caractères : {{ userInput.length }}</v-card-subtitle>
          <v-alert v-if="containsPokemon" type="success" class="mt-2">
            Vous avez mentionné "Pokémon" !
          </v-alert>
          <v-alert v-if="userInput.length === maxLength" type="warning" class="mt-2">
            La saisie a atteint la limite maximale et a été réinitialisée.
          </v-alert>
        </v-card-text>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
import { ref, watch } from 'vue';

// Variable réactive pour la saisie utilisateur
const userInput = ref('');

// Longueur maximale autorisée
const maxLength = 50;

// Variable réactive pour indiquer si "Pokémon" est présent
const containsPokemon = ref(false);

// Watcher pour surveiller la saisie utilisateur
watch(userInput, (newValue) => {
  // Vérifie si "Pokémon" est mentionné
  containsPokemon.value = newValue.toLowerCase().includes('pokémon');

  // Réinitialise la saisie si elle dépasse la longueur maximale
  if (newValue.length > maxLength) {
    userInput.value = '';
  }
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
