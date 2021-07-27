<template>
  <div id="app">
  <h1>Анекдоты</h1>
  <list 
    v-bind:anecdotes="anecdotes"
  />
  </div>
</template>

<script>
import list from '@/components/list'
export default {
  data() {
    return {
      anecdotes: [
        {id: 1, text: 'lalala', liked: false },
        {id: 2, text: 'ldddffalala', liked: false },
        {id: 3, text: 'laladfdgla', liked: false },
      ]
    }
  },
  name: 'App',
  components: {
    list
  }
}
</script>

<style>
body {
  padding: 10px
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
