<template>
  <v-container max-width="700">
    <h1>Exercice 4</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>
          Utiliser la directive <code>v-model</code> pour lier
          le champ de texte <code>&lt;v-text-field&gt;</code> à une
          variable <code>userInput</code>.
        </li>
        <li>
          Utiliser une <strong>propriété calculée (computed)</strong>
          pour afficher
          dynamiquement le nombre de caractères restants
          par rapport à la limite de caractères <code>MAX_LENGTH</code>.
        </li>
        <li>
          Afficher dynamiquement la valeur de la <strong>propriété
          calculée</strong> à la place du texte <code>*** CARACTÈRES
          RESTANTS ***</code>.
        </li>
        <li>
          Afficher le message d'avertissement <code>&lt;v-alert&gt;</code>
          si l'utilisateur dépasse la limite de caractères.
        </li>
        <li>
          Utiliser une <strong>référence (ref)</strong> pour accéder
          au champ de texte <code>&lt;v-text-field&gt;</code>
          et mettre le focus dessus en cliquant sur
          le bouton <code>Activer le champ de texte</code>.
        </li>

      </ul>
    </div>
    <v-divider class="my-4"/>
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card class="mx-auto my-6 pa-2" max-width="500">
        <v-card-title>Saisie avec limite de caractères</v-card-title>

        <v-card-subtitle>
          Caractères restants :
          <strong>*** CARACTÈRES RESTANTS ***</strong>
        </v-card-subtitle>

        <v-card-text>
          <v-alert type="error" class="mb-2">
            Vous avez atteint la limite maximale de caractères !
          </v-alert>

          <v-text-field
            outlined
            rows="2"
            label="Tapez votre texte ici"
            :counter="MAX_LENGTH"
          />
        </v-card-text>

        <v-card-actions>
          <v-btn color="primary">
            Activer le champ de texte
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
import {ref} from 'vue';

// Constante pour la limite de caractères
const MAX_LENGTH = 20;
// Variable réactive pour le texte saisi
const userInput = ref('');

</script>
