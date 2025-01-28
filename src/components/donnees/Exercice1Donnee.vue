<template>
  <h1>Exercice 1</h1>
  <h2>Objectifs</h2>
  <ul>
    <li>Rendre le titre de la carte dynamique en utilisant le texte de la variable <v-code>title</v-code> pour remplacer <v-code>*** TITRE ***</v-code>.</li>
    <li>Rendre la description de la carte dynamique en utilisant le texte de la variable <v-code>description</v-code> pour remplacer <v-code>*** DESCRIPTION ***</v-code>.</li>
    <li>Changer dynamiquement la couleur du texte de la description en
      fonction de
      la valeur de <v-code>isHighlighted</v-code> :
      <ul>
        <li><v-code>blue</v-code> si <v-code>isHighlighted</v-code> est <v-code>true</v-code>.</li>
        <li><v-code>black</v-code> si <v-code>isHighlighted</v-code> est
          <v-code>false</v-code>.</li>
      </ul>
    </li>
    <li>Ajouter un événement <v-code>click</v-code> sur le bouton qui inverse
      la valeur <v-code>true/false</v-code> de <v-code>isHighlighted
      </v-code>.</li>
    <li>Faire en sorte que le texte du bouton change dynamiquement :
      <ul>
        <li>Afficher <v-code>Réinitialiser la couleur</v-code> si <v-code>
          isHighlighted</v-code> est <v-code>true</v-code>.</li>
        <li>Afficher <v-code>Mettre en surbrillance</v-code> si <v-code>
          isHighlighted</v-code> est <v-code>false</v-code>.</li>
      </ul>
    </li>
    <li>
      <strong>Suggestion</strong> : Utilisez des outils comme <strong>Vue
      DevTools</strong> pour modifier les valeurs de vos données et observer
      les changements dynamiques sur la carte.
    </li>
    <li>
      <strong>Astuce :</strong> Vous pourriez avoir besoin de rendre
      <strong>réactives</strong> les variables
      <v-code>isHighlighted</v-code>, <v-code>title</v-code> et <v-code>
      description</v-code>.
    </li>
  </ul>
  <v-divider class="my-6" />
  <h2>Code à modifier</h2>
</template>
<script setup lang="ts">
</script>
