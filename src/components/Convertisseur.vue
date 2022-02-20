<template>
  <!--Image de fond -->
  <div :style="{ 'background-image': 'url(./assets/photo.jpg)' }"></div>
  <!--Titre-->
  <h1>g/l => mmol/l</h1>
  <div class="container">
    <!--Zone input-->
    <fieldset class="saisie">
      <legend>Veuillez saisir la glycémie</legend>
      <input placeholder="saisie" v-model="glycemie" />

      <!--Menu déroulant-->

      <select class="menu" v-model="choix">
        <option value="grammes">Grammes</option>
        <option value="mmol">Mmol</option>
      </select>

      <!--Bouton conversion-->

      <button v-on:click="calcul">Conversion</button>
    </fieldset>

    <!--Zone résultat-->
    <fieldset class="result">
      {{ result }}
      <legend>Votre résultat</legend>
    </fieldset>
  </div>
</template>

<script>
export default {
  name: "Convertisseur",
  data() {
    return {
      value: "",
      glycemie: "",
      choix: "",
      result: 0,
    };
  },

  methods: {
    calcul() {
      if (this.choix === "grammes") {
        this.result = this.glycemie * 5.5 + " mmol";
      } else if (this.choix === "mmol") {
        this.result = this.glycemie * 0.18 + " grammes";
      }
      return this.result;
    },
  },
};
</script>
<style scoped>
h1 {
  margin-bottom: 100px;
  margin-left: 100px;
  text-align: center;
  font-style: italic;
  font-size: 3em;
}
.saisie {
  width: 600px;
  margin-left: 500px;
  border-color: rgb(204, 200, 200);
}
.result {
  margin-top: 20px;
  width: 600px;
  margin-left: 500px;
  border-color: rgb(204, 200, 200);
}
input {
  margin-left: -150px;
  margin-right: 20px;
}
.menu {
  margin-top: -300px;
  margin-right: 20px;
}
</style>
