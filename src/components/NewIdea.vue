<template>
  <div class="form">
    <form  v-on:submit.prevent="$emit('add-idea', submitIdea())">
      <input type="text" id='title' v-model='title' v-on:change='handleChange'/>
      <input type="text" id='body' v-model='body' v-on:change='handleChange'/>
      <input type="submit">
    </form>
  </div>
</template>

<script>
import uuid from 'uuid';
export default {
  name: 'NewIdea',
  data() {
    return {
      title: 'the title',
      body: 'the body'
    }
  },
  methods: {
    handleChange(e) {
      this[e.target.id] = e.target.value
    },
    submitIdea() {
      const idea = {
        title: this.title,
        body: this.body,
        id: uuid.v4()
      }
      return idea
    }
  }
}
</script>

<style scoped>

</style>