<template>
  <div class="calculator">
    <label>Addition</label>
    <input :value="first" @input="first = $event.target.value" />
    <input :value="second" @input="second = $event.target.value" />
    total : {{ total() }}
  </div>
</template>
<script>
export default {
  data() {
    return {
      first: 0,
      second: 0,
    };
  },
  methods: {
    total() {
      return this.first + this.second;
    },
  },
};
</script>