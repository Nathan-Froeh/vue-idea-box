<template>
  <div id="form">
    <form action="">
      <input type="text" name='title' v-model='title' v-on:change='handleChange'/>
      <input type="text" name='body' v-model='body' v-on:change='handleChange'/>
      <input type="submit" value="submit">
    </form>
  </div>
</template>

<script>
export default {
  name: 'form',
  data() {
    return {
      title: 'the title',
      body: 'the body'
    }
  },
  methods: {
    handleChange(e) {
      this[e.target.name] = e.target.value
    }
  }
}
</script>

<style scoped>

</style>