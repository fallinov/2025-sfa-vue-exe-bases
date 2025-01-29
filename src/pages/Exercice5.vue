<template>
  <v-container max-width="700">
    <h1>Exercice 5</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>
          Apprendre à utiliser les <strong>watchers</strong>
          pour surveiller les changements d’une variable réactive.
        </li>
        <li>
          Afficher dynamiquement le nombre de caractères saisis
          dans la variable <code>userInput</code> à la place de
          <code>*** CARACTÈRES SAISIS ***</code>.
        </li>
        <li>
          Surveiller avec un <strong>watcher</strong>
          la saisie utilisateur, la variable
          <code>userInput</code>
          et afficher un message <code>&lt;v-alert&gt;</code>
          lorsque le texte contient le mot <strong>"Pokémon"</strong>
          en ignorant la casse (majuscules/minuscules).
        </li>
        <li>
          Dans le même <strong>watcher</strong>, réinitialiser
          automatiquement la saisie, mettre une chaîne vide,
          si elle dépasse la longueur maximale <code>MAX_LENGTH</code>.
        </li>
      </ul>
    </div>
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
import { ref } from 'vue';

// Variable réactive pour la saisie utilisateur
const userInput = ref('');

// Longueur maximale autorisée
const MAX_LENGTH = 20;

// Variable réactive pour indiquer si "Pokémon" est présent
const containsPokemon = ref(false);
</script>
