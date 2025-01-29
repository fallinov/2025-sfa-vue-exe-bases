<template>
  <v-container max-width="700">
    <!-- Bloc d'objectifs pédagogiques -->
    <h1>Exercice 2</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>
          Permettre à l'utilisateur de <strong>modifier dynamiquement</strong> le
          titre et la description de la carte via un formulaire.
        </li>
        <li>
          Modifier les deux champs de formulaire <code>&lt;v-text
          -field /&gt;</code> et <code>v-textarea /&gt;</code> en utilisant
          la directive <code>v-model</code> pour les
          lier aux données <code>title</code> et <code>description</code>.
        </li>
        <li>
          Afficher dynamiquement, en live, les valeurs de <code>title
        </code> et <code>description</code> sur la carte à la place de
        <code>*** TITRE ***</code> et <code>*** DESCRIPTION ***</code>.
        </li>
      </ul>
    </div>
    <v-divider class="my-4"/>
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>

      <!-- Formulaire pour modifier les données -->
      <v-form class="my-6">
        <!-- Ajoutez ici une liaison dynamique avec la variable title -->
        <v-text-field
          label="Modifier le titre"
          placeholder="Entrez un nouveau titre"
          outlined
          class="mb-4"
        />
        <!-- Ajoutez ici une liaison dynamique avec la variable description -->
        <v-textarea
          label="Modifier la description"
          placeholder="Entrez une nouvelle description"
          outlined
          rows="3"
        />
      </v-form>

      <!-- Carte dynamique -->
      <v-card class="mx-auto my-6 pa-2" max-width="400">
        <!-- Titre dynamique -->
        <v-card-title>*** TITRE ***</v-card-title>

        <!-- Description dynamique -->
        <v-card-subtitle>
          *** DESCRIPTION ***
        </v-card-subtitle>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
// Données préparées pour l'exercice
const title = "Bienvenue à l'exercice 2"
const description = "Cet exercice teste la gestion des événements et l'interaction avec les formulaires."
</script>

