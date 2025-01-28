<template>
  <v-container max-width="700">
    <h1>Exercice 3</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>Créer une liste dynamique de Pokémons basée sur la variable
          <code>pokemons</code> qui contient un <strong>tableau
            de noms de Pokémons</strong>.
        </li>
        <li>Utiliser la directive <code>v-for</code> pour parcourir le tableau
          et créer les éléments de la liste <code>&lt;v-list-item&gt;</code>.
        </li>
        <li>
          Utiliser l'index, position dans le tableau,
          comme clé <code>:key ="index"</code>
          de la directive <code>v-for</code> pour identifier chaque élément
          de la liste.
        </li>
        <li>
          Remplacer le texte <code>*** POKEMON ***</code> par le nom du Pokémon
          parcourus dans la boucle <code>v-for</code>.
        </li>
        <li>Ecouter l'événement <code>click</code> sur le bouton de suppression
          pour appeler la fonction <code>removePokemon(index)</code> et ainsi
          supprimer le Pokémon.
        </li>
        <li>Afficher le message <code>"La liste est vide"</code> uniquement
          si le tableau ne contient plus de Pokémons. Sinon, afficher la liste
          des Pokémons.
        </li>
      </ul>
    </div>
    <v-divider class="my-4"/>
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>
      <v-card
        class="mx-auto my-6 pa-2"
        max-width="300"
      >
        <v-card-title>Liste de Pokémons</v-card-title>

        <v-card-subtitle class="text-center">
          La liste est vide.
        </v-card-subtitle>

        <v-list>
          <v-list-item>
            <v-list-item-title>
              *** POKEMON ***
            </v-list-item-title>

            <template v-slot:append>
              <v-btn
                icon="mdi-delete"
                variant="text"
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

// Tableau des Pokémons réactif
const pokemons = ref([
  "Pikachu",
  "Bulbizarre",
  "Salamèche",
  "Carapuce",
  "Rondoudou"
]);

/**
 * Fonction qui supprime le Pokémon à l'index donné.
 * @param {number} index - Index, position, du Pokémon à supprimer.
 */
function removePokemon(index) {
  pokemons.value.splice(index, 1);
}
</script>

