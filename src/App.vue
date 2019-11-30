<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <NewIdea v-on:add-idea='addIdea'/>
    <IdeaContainer v-bind:ideas='ideas'/>
  </div>
</template>

<script>
import NewIdea from './components/NewIdea';
import IdeaContainer from './components/IdeaContainer';

export default {
  name: 'app',
  components: {
    NewIdea,
    IdeaContainer
  },
  data() {
    return {
      ideas: [{title: 'hi', body: 'sup', id: 1}]
    }
  },
  methods: {
    addIdea(idea) {
      this.ideas.push(idea)
    }
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
