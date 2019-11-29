<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Form/>
  </div>
</template>

<script>
import Form from './components/Form';

export default {
  name: 'app',
  components: {
    Form
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
