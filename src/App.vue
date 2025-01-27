<template>
  <v-app class="bg-grey-lighten-5">
    <v-navigation-drawer v-model="drawer">
      <v-list density="compact" item-props :items="items" nav />

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
    to: '/exercice1',
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
    subtitle: 'Composants, props et emits',
    prependIcon: 'mdi-cube-outline', // Icône pour représenter les composants
    to: '/exercice5',
  },
]);
</script>
