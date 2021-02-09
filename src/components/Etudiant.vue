<template>
  <div class="etudiant">
    <span>Il y'a : {{ counter }} Etudiants</span>
     <table>
       <thead>
         <th>#</th>
         <th>Nom</th>
         <th>Prenom</th>
         <th>Age</th>
       </thead>
       <tbody>
         <tr v-for="(Etudiant, index) in Etudiants" :key="index">
           <td>{{index }}</td>
           <td>{{ Etudiant.nom }}</td>
           <td>{{ Etudiant.prenom }}</td>
           <td>{{ Etudiant.age + 1}}</td>
         </tr>
       </tbody>
     </table>
    <button @click="addEtudiant">Ajouter un etudiant</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Etudiants: []
    }
  },
  props: {
    nom: String,
    prenom: String,
    age: In
  },
  methods: {
    addEtudiant(){
      this.Etudiants.push({
        nom: "Sylla",
        prenom: "Ousmane",
        age: 17
      });
    }
  },
  computed: {
    counter(){
     return this.Etudiants.length
    }
  },
  mounted() {
    this.Etudiants.push({
      nom: this.nom,
      prenom: this.prenom,
      age: this.age,
    })
  },
}
</script>