<template>
  <v-container class="pa-6">
    <!-- Bloc d'objectifs pédagogiques -->
    <h1>Exercice 1</h1>
    <h2>Objectifs</h2>
    <ul>
      <li>Rendre le titre de la carte dynamique en utilisant le texte de la
        variable <code>title</code>.
      </li>
      <li>Rendre la description de la carte dynamique en utilisant le texte de
        la variable <code>description</code>.
      </li>
      <li>Changer dynamiquement la couleur de la description en fonction de la
        valeur de la variable <code>isHighlighted</code> :
        <ul>
          <li>Si <code>isHighlighted</code> est à <code>true</code>, la couleur
            doit être bleue.
          </li>
          <li>Sinon, la couleur doit être noire.</li>
        </ul>
      </li>
      <li>Ajouter un bouton qui modifie la valeur de <code>isHighlighted</code>
        lorsqu’il est cliqué.
      </li>
      <li>Faire en sorte que le texte du bouton change dynamiquement :
        <ul>
          <li>Afficher "Réinitialiser la couleur" si <code>isHighlighted</code>
            est à <code>true</code>.
          </li>
          <li>Afficher "Mettre en surbrillance" sinon.</li>
        </ul>
      </li>
    </ul>

    <!-- Carte statique à transformer -->
    <v-card class="mx-auto" max-width="400">
      <!-- Titre statique (remplacer par un contenu dynamique) -->
      <v-card-title>Bienvenue à l'exercice 1</v-card-title>

      <!-- Description statique (remplacer par un contenu dynamique avec une liaison de style) -->
      <v-card-subtitle style="color: black;">
        Cet exercice teste le rendu déclaratif et les liaisons d'attributs.
      </v-card-subtitle>

      <!-- Bouton statique (ajouter un événement pour le rendre fonctionnel) -->
      <v-card-actions>
        <v-btn color="primary">
          Mettre en surbrillance
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script setup>
import {ref} from 'vue';

// Données préparées pour l'exercice
const title = ref("Bienvenue à l'exercice 1");
const description = ref("Cet exercice teste le rendu déclaratif et les liaisons d'attributs.");
const isHighlighted = ref(false);

// Fonction pour basculer la surbrillance
const toggleHighlight = () => {
  isHighlighted.value = !isHighlighted.value;
};
</script>

<style scoped>
.v-card {
  margin-top: 20px;
}
</style>
