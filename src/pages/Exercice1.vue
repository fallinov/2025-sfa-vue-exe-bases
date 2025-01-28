<template>
  <v-container max-width="700">
    <!-- Bloc d'objectifs pédagogiques -->
    <h1>Exercice 1</h1>
    <div class="exe-objectifs">
      <h2>Objectifs</h2>
      <ul>
        <li>
          Rendre le <strong>titre de la carte dynamique</strong> en utilisant le
          texte de la
          variable <code>title</code> pour remplacer <code>*** TITRE ***</code>.
        </li>
        <li>
          Rendre la <strong>description de la carte dynamique</strong> en
          utilisant le texte de
          la variable <code>description</code>
          pour remplacer <code>*** DESCRIPTION ***</code>.
        </li>
        <li>
          Changer dynamiquement la <strong>couleur du texte</strong> de la
          description en
          fonction de
          la valeur de <code>isHighlighted</code> :
          <ul>
            <li><code>blue</code> si <code>isHighlighted</code> est
              <code>true</code>.
            </li>
            <li><code>black</code> si <code>isHighlighted</code> est
              <code>false</code>.
            </li>
          </ul>
        </li>
        <li>
          Ajouter un événement <code>click</code> sur le <strong>bouton</strong>
          qui inverse
          la valeur <code>true/false</code> de <code>isHighlighted</code>.
        </li>
        <li>
          Faire en sorte que le <strong>texte du bouton</strong> change
          dynamiquement :
          <ul>
            <li>Afficher <code>"Réinitialiser la couleur"</code> si <code>
              isHighlighted</code> est <code>true</code>.
            </li>
            <li>Afficher <code>"Mettre en surbrillance"</code> si <code>
              isHighlighted</code> est <code>false</code>.
            </li>
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
          <code>isHighlighted</code>, <code>title</code> et <code>
          description</code>.
        </li>
      </ul>
    </div>
    <v-divider class="my-4"/>
    <div class="exe-zone">
      <h2>Zone d'exercice</h2>

      <!-- Carte statique à transformer -->
      <v-card class="mx-auto my-6 pa-2" max-width="400">
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
    </div>
  </v-container>
</template>

<script setup>
// Données préparées pour l'exercice
// SUGGESTION : Pensez à rendre ces données réactives pour qu'elles puissent être mises à jour dynamiquement.
const title = "Bienvenue à l'exercice 1";
const description = "Cet exercice teste le rendu déclaratif et les liaisons d'attributs.";
const isHighlighted = false;
</script>
