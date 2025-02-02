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
        Créer et appliquer une classe CSS conditionnelle <code>.done</code>
        au titre de la tâche terminée <code>&lt;v-list-item-title&gt;</code>
        pour la barrer à l'aide de CSS
        <code>text-decoration: line-through</code>.
      </li>
      <li>
        Pour ajouter une nouvelle tâche, utiliser la méthode
        <code>addTask()</code>. Appeler cette méthode lors du
        clic sur le bouton <code>Ajouter</code>.
      </li>
      <li>
        Remplacer le texte <code>*** Nouvelle tâche ***</code>
        par la valeur saisie par l'utlisateur dans le champ de texte.
        <code>&lt;v-text-field&gt;</code>.
        Utiliser la directive <code>v-model</code> pour lier la valeur
        du champ de texte à la propriété <code>newTask</code>.
      </li>
      <li>
        Créer une propriété calculée <code>sortTasks()</code>
        qui retourne les tâches triées par ordre de création, en affichant
        les tâches non terminées en premier.
        <br>
        Utiliser la méthode <code>sort()</code> sur le tableau <code>tasks</code>
      </li>
      <li>
        Utilser la propriété calculée <code>sortTasks()</code>
        dans la directive <code>v-for</code> pour afficher les tâches.
      </li>
    </ul>


    <ul>
      <li>Les tâches à faire seront toujours affichées en premier.</li>
      <li>Une case, en bas de liste, permettra de masquer les tâches terminées.</li>
    </ul>
  </div>
</template>
<script setup lang="ts">
</script>
