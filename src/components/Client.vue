<template lang="fr">
  <div class="client">
    
    <h2>{{msg}}</h2>
    <h3>Bonjour : {{Personne.nom}} {{Personne.prenom}}</h3>
    <form>
      <label>Nom:</label><input type="text" v-model="Personne.nom"><br>
      <label>Prenom:</label><input type="text" v-model="Personne.prenom"><br>
      <label>Message:</label>
      <textarea v-model="msg">
        
      </textarea>
      <br>
    </form>
  </div>
</template>

<script>
export default {
  name: "Client",
  data() {
    return {
      Personne: {
        nom: "Sylla",
        prenom: "Ousmnae"
      },
      msg: "Bienvenue chez Bee School"
    }
  },
}
</script>