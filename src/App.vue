<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>{{name}}</h1>
  <button @click="append" v-bind:disabled="isDisabled">Append</button>
  <div v-html="title"></div>
<div v-bind:id="ID" v-bind:class="container">Hello</div>
<div :id="ID" :class="container">Hello</div>
</template>

<script>
export default {
  name: 'App',
data(){
  return {
    name : "Rushikesh",
    title :"<h1 style=color:red>Hello</h1>",
    ID : "specialOne",
    container : "wrapper",
    isDisabled : true,
  }
}
,
methods : {
append(){
  this.name+=" Tarapure" 
}
}
}
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

.wrapper{
  border : 1px solid black;
  width : 50%;
}
</style>
