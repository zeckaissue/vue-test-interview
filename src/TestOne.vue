<template>
  <div>
    <div>Fruit selectionné: {{ selectedDemo && selectedDemo.label }}</div>
    <div class="items">
      <div v-for="item in items" :key="item.id">
        {{ item.label }}
        <button @click="choose(item)">choisir</button>
      </div>
    </div>
    <div>Fruit selectionné: {{ selected && selected.label }}</div>
    <custom-selector :option="items" v-model="selected" />
  </div>
</template>
<script>
import CustomSelector from "./components/CustomSelector.vue";

export default {
  components: {
    CustomSelector,
  },
  data() {
    return {
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
  },
};
</script>
<style lang="scss" scoped>
.items {
  margin-bottom: 32px;
}
</style>
