<template>
  <v-container>
    <!-- Bloc d'objectifs pédagogiques -->
    <h1>Exercice 1</h1>
    <h2>Objectifs</h2>
    <ul>
      <li>Rendre le titre de la carte dynamique en utilisant le texte de la variable <v-code>title</v-code> pour remplacer <v-code>*** TITRE ***</v-code>.</li>
      <li>Rendre la description de la carte dynamique en utilisant le texte de la variable <v-code>description</v-code> pour remplacer <v-code>*** DESCRIPTION ***</v-code>.</li>
      <li>Changer dynamiquement la couleur de la description en fonction de la valeur de <v-code>isHighlighted</v-code> :</li>
      <ul>
        <li>Bleu si <v-code>isHighlighted</v-code> est <v-code>true</v-code>.</li>
        <li>Noir sinon.</li>
      </ul>
      <li>Ajouter un bouton qui modifie la valeur de <v-code>isHighlighted</v-code> lorsqu’il est cliqué.</li>
      <li>Faire en sorte que le texte du bouton change dynamiquement :</li>
      <ul>
        <li>Afficher "Réinitialiser la couleur" si <v-code>isHighlighted</v-code> est <v-code>true</v-code>.</li>
        <li>Afficher "Mettre en surbrillance" sinon.</li>
      </ul>
      <li>
        **Suggestion :** Utilisez des outils comme <v-code>Vue DevTools</v-code> pour observer les changements dynamiques dans les données pendant que vous interagissez avec la carte.
      </li>
      <li>
        **Astuce :** Vous pourriez avoir besoin de rendre les variables <v-code>isHighlighted</v-code>, <v-code>title</v-code> et <v-code>description</v-code> réactives. Pensez aux outils Vue.js adaptés !
      </li>
    </ul>
    <v-divider class="my-6" />
    <h2>Code à modifier</h2>

    <!-- Carte statique à transformer -->
    <v-card class="mx-auto pa-2" max-width="400">
      <!-- Remplacez *** TITRE *** par un contenu dynamique -->
      <v-card-title>*** TITRE ***</v-card-title>

      <!-- Remplacez *** DESCRIPTION *** par un contenu dynamique avec une liaison de style -->
      <v-card-subtitle style="color: black;">
        *** DESCRIPTION ***
      </v-card-subtitle>

      <!-- Rendez ce bouton fonctionnel pour changer la couleur -->
      <v-card-actions>
        <v-btn color="primary">
          Mettre en surbrillance
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script setup>
// Données préparées pour l'exercice
const title = "Bienvenue à l'exercice 1";
const description = "Cet exercice teste le rendu déclaratif et les liaisons d'attributs.";
const isHighlighted = false;

// SUGGESTION : Pensez à rendre ces données réactives pour qu'elles puissent être mises à jour dynamiquement.
</script>
