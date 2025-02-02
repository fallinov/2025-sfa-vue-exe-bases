<template>
  <h1>Exercice 6</h1>
  <div class="exe-objectifs">
    <h2>Objectifs</h2>
    <ul>
      <li>
        Parcourir le tableau <em>réactif</em> des tâches <code>tasks</code>
        avec la directive <code>v-for</code>
        et les afficher dans la liste en répétant l'élément
        <code>&lt;v-list-item&gt;</code>.
        <br>
        Utiliser la propriété <code>key</code> pour identifier chaque tâche.
      </li>
      <li>
        Afficher le titre de la tâche dans le composant
        <code>&lt;v-list-item-title&gt;</code> à la place
        du texte <code>*** Titre de la tâche ***</code>.
      </li>
      <li>
        Afficher la date de création dans le composant
        <code>&lt;v-list-item-subtitle&gt;</code> à la place
        du texte <code>*** Date ***</code>
        et <code>*** Heure ***</code>.
        <ul>
          <li>
            Pour créer une date à partir du <em>timestamp</em> de la date de création,
            utiliser la méthode <code>new Date(task.date)</code>.
          </li>
          <li>
            Utiliser la méthode <code>toLocaleDateString()</code> pour récupérer
            la date en format <code>jj/mm/aaaa</code> et la méthode
            <code>toLocaleTimeString()</code> pour récupérer l'heure en format
            <code>hh:mm:ss</code>.
          </li>
        </ul>
      </li>

      <li>
        Afficher un message si le tableau <code>tasks</code> est vide
        en affichant le composant <code>&lt;v-card-subtitle&gt;</code>
        qui contient le message <code>Il n'y a pas de tâches... chanceux !
        😄</code>
      </li>
      <li>
        Rendre dynamique la case à cocher pour marquer une tâche comme
        terminée ou non. Utiliser la directive <code>v-model</code> pour
        lier la propriété <code>completed</code> de chaque tâche au composant
        <code>&lt;v-checkbox-btn&gt;</code>.
      </li>
      <li>
        Créer et appliquer une classe CSS conditionnelle <code>done</code>
        au titre des tâches terminées <code>&lt;v-list-item-title&gt;</code>
        pour la barrer à l'aide de CSS
        <code>text-decoration: line-through</code>.
      </li>
      <li>
        Pour ajouter une nouvelle tâche, utiliser la méthode
        <code>addTask()</code>. Appeler cette méthode lors du
        clic sur le bouton <code>Ajouter</code>.
      </li>
      <li>
        Dans la méthode <code>addTask()</code>, remplacer le texte <code>***
        Nouvelle tâche ***</code> par la valeur saisie par l'utlisateur dans
        le champ de texte <code>&lt;v-text-field&gt;</code>.
        Utiliser la directive <code>v-model</code> pour lier la valeur
        du champ de texte à la donnée réactive <code>newTask</code>.
      </li>
      <li>
        Créer une propriété calculée <code>sortTasks()</code>
        qui retourne les tâches triées par date de création, de la plus récente
        à la plus ancienne.
        <br>
        Utiliser la méthode <code>sort()</code> pour trier les tâches.
      </li>
      <li>
        Utilser la propriété calculée <code>sortTasks()</code>
        dans la directive <code>v-for</code> pour afficher les tâches triées par
        date de création.
      </li>
    </ul>
  </div>
</template>
<script setup lang="ts">
</script>
