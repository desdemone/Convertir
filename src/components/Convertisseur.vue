<template>
  <!--Image de fond -->
  <div :style="{ 'background-image': 'url(./assets/photo.jpg)' }"></div>
  <!--Titre-->
  <h1>Conversion g/l => mmol/l</h1>
  <!--Menu déroulant-->
  <div class="bloc">
    <select v-model="choix">
      <option value="grammes">Grammes</option>
      <option value="mmol">Mmol</option>
    </select>
    <!--Bouton conversion-->
    <button v-on:click="calcul">Conversion</button>
  </div>
  <!--Zone input-->
  <div class="bloc1">
    <div class="input">
      <input placeholder="saisissez la glycémie" v-model="glycemie" />
    </div>
  </div>
  <!--Zone résultat-->
  <p class="result"><strong> Résultat :</strong> {{ result }}</p>
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
      return this.result.toFixed(2);
    },
  },
};
</script>
<style scoped>
.bloc {
  margin-left: 400px;
}

button {
  margin-left: 20px;
  margin-top: 100px;
}

.bloc1 {
  margin-top: -20px;
}

h1 {
  margin-bottom: 100px;
  text-align: center;
  font-style: italic;
  font-size: 60px;
}
</style>
