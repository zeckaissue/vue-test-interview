<template>
  <div id="app">
    <h2>Test 1 (v-model)</h2>
    <p>
      Faire fonctionner le composant "custom-selector" comme l'exemple affiché
    </p>
    <test-one />
    <hr class="sep" />
    <h2>Test 2 - Correction de code</h2>
    <p>
      Corrigez le composant "TestTwo" afin qu'il fonctionne et respecte les
      bonnes pratiques
    </p>
    <test-two />
    <hr class="sep" />
    <h2>Test 3 - Intégration</h2>
    <ul>
      <li>
        Mettre en forme le bloc suivant afin qu'il corresponde à la l'image.
      </li>
      <li>
        Vous ne devez pas toucher au composant CmsBlock, mais uniquement ajouter
        du style css dans le composant "TestThree"
      </li>
      <li>
        La balise style du composant "TestThree" doit garder l'attribut scoped
      </li>
    </ul>
    <div>
      <img src="goal.png" />
    </div>
    <br />

    <test-three />
  </div>
</template>

<script>
import TestOne from "./TestOne.vue";
import TestTwo from "./TestTwo.vue";
import TestThree from "./TestThree.vue";

export default {
  name: "App",
  components: {
    TestThree,
    TestOne,
    TestTwo,
  },
  data() {
    return {
      first: 0,
      second: 0,
      selected: null,
      selectedDemo: null,
      items: [
        { label: "Pomme", id: 1 },
        { label: "Orange", id: 2 },
        { label: "Mandarine", id: 3 },
      ],
    };
  },
  methods: {
    choose(item) {
      this.selectedDemo = item;
    },
    total() {
      return this.first + this.second;
    },
  },
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.sep {
  margin: 120px 0;
}
img {
  max-width: 100%;
  height: auto;
  display: block;
  margin: auto;
}
</style>
