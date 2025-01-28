<template>
  <v-container max-width="700">
    <h1>Exercice 3</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>Créer une liste dynamique affichée sur une carte à partir d’un
          tableau de données.
        </li>
        <li>Utiliser la directive <code>v-for</code> pour parcourir et afficher
          les éléments de la liste.
        </li>
        <li>Ajouter un bouton permettant de supprimer un élément spécifique de
          la liste.
        </li>
        <li>Afficher un message <strong>"La liste est vide"</strong> si le
          tableau ne contient plus d’éléments.
        </li>
        <li><strong>Suggestion :</strong> Testez votre travail avec différents
          jeux de données.
        </li>
      </ul>
    </div>
    <v-divider class="my-4"/>
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card
        class="mx-auto my-6 pa-2"
        max-width="300"
        prepend-icon="mdi-pokeball"
        title="Pokémons"
      >
        <v-card-subtitle v-if="pokemons.length === 0" class="text-center">
          La liste est vide.
        </v-card-subtitle>
        <v-list v-else>
          <v-list-item
            v-for="(pokemon, index) in pokemons"
            :key="index"
          >
            <v-list-item-title>
              {{ pokemon }}
            </v-list-item-title>
            <template v-slot:append>
              <v-btn
                icon="mdi-delete"
                variant="text"
                @click="removePokemon(index)"
              ></v-btn>
            </template>
          </v-list-item>
        </v-list>
      </v-card>
    </div>
  </v-container>
</template>

<script setup>
import {ref} from 'vue';

const pokemons = ref(["Pikachu", "Bulbizarre", "Salamèche", "Carapuce", "Rondoudou"]);

const removePokemon = (index) => {
  pokemons.value.splice(index, 1);
};
</script>

