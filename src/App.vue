<template>
  <v-app class="bg-grey-lighten-5 pa-0">
    <v-navigation-drawer v-model="drawer" class="pa-0">
      <v-list item-props :items="items" nav />
      <!--      <template #append>
          <v-list-item
            class="ma-2"
            link
            nav
            prepend-icon="mdi-cog-outline"
            title="Settings"
          />
        </template>-->
    </v-navigation-drawer>

    <v-app-bar border="b" class="ps-4" flat>
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <v-app-bar-title>Les bases de Vue.js</v-app-bar-title>
    </v-app-bar>

    <v-main>
      <router-view  />
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from 'vue'

const drawer = ref(true)

const items = ref([
  {
    title: 'Exercice 1',
    subtitle: 'Rendu déclaratif et liaisons d’attributs',
    prependIcon: 'mdi-pencil-outline', // Icône pertinente pour l'exercice
    to: '/',
  },
  {
    title: 'Exercice 2',
    subtitle: 'Gestion des événements et champs de formulaire',
    prependIcon: 'mdi-form-select', // Icône pertinente pour un formulaire
    to: '/exercice2',
  },
  {
    title: 'Exercice 3',
    subtitle: 'Rendu conditionnel et liste dynamique',
    prependIcon: 'mdi-format-list-bulleted', // Icône pour une liste
    to: '/exercice3',
  },
  {
    title: 'Exercice 4',
    subtitle: 'Propriétés calculées et refs',
    prependIcon: 'mdi-clock-outline', // Icône pour un calcul lié au temps
    to: '/exercice4',
  },
  {
    title: 'Exercice 5',
    subtitle: 'Observateurs et watchers',
    prependIcon: 'mdi-eye-outline', // Icône pour un observateur
    to: '/exercice5',
  },
  {
    title: 'Exercice 6',
    subtitle: 'Liste de tâches',
    prependIcon: 'mdi-check-all', // Icône pour une liste de tâches
    to: '/exercice6',
  },
  {
    title: 'Exercice 7',
    subtitle: 'Cycle de vie de Vue.js',
    prependIcon: 'mdi-lifebuoy', // Icône pour le cycle de vie
    to: '/exercice7',
  },
  {
    title: 'Exercice 8',
    subtitle: 'Composants',
    prependIcon: 'mdi-view-module', // Icône pour un composant
    to: '/exercice8',
  },
  {
    title: 'Exercice 9',
    subtitle: 'Slots et contenu nommé',
    prependIcon: 'mdi-card-text-outline', // Icône pour un slot
    to: '/exercice9',
  },/*
  {
    title: 'Exercice 10',
    subtitle: 'Composition API',
    prependIcon: 'mdi-code-tags', // Icône pour la composition
    to: '/exercice10',
  },*/

]);
</script>
