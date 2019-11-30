<template>
  <main>
    <ul>
      <li v-for="{title, body, id} in ideas" v-bind:key="id">
        <p>{{title}}</p>
        <p>{{body}}</p>
      </li>
    </ul>

  </main>
</template>

<script>
export default {
  name: 'IdeaContainer',
  props: ["ideas"]
}
</script>

<style scoped>

</style>