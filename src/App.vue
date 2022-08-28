<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>{{ name }}</h1>
  <button @click="append" v-bind:disabled="isDisabled">Append</button>
  <div v-html="title"></div>
  <div v-bind:id="ID" v-bind:class="[`container`, `danger`]">Hello</div>
  <div :id="ID" class="underline" :class="status ? danger : safe">
    Conditional
  </div>
  <div :class="[!status && 'danger']">Color it 2</div>
  <div :style="{ color }">InLine styling Color it</div>
  <h2 v-if="num > 0">This is +ve</h2>
  <h2 v-else-if="num < 0">This is -ve</h2>
  <h2 v-else> This is Zero</h2>
  <div :style="stylishObject">InLine styling Color it</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Rushikesh",
      title: "<h1 style=color:red>Hello</h1>",
      ID: "specialOne",
      container: "wrapper",
      isDisabled: true,
      status: false,
      danger: "danger",
      safe: "safe",
      color: "violet",
      stylishObject: {
        backgroundColor: "yellow",
        color: "orange",
        border: "1px solid violet",
        padding: "20px",
      },
      num: -1,
    };
  },
  methods: {
    append() {
      this.name += " Tarapure";
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.wrapper {
  border: 1px solid black;
  width: 50%;
}

.danger {
  background-color: tomato;
}

.safe {
  background-color: green;
}
</style>
