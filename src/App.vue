<template>
  <div id="app">
  <h1>Jokes</h1>
  <h2>Test by Maria Gileto</h2>
  <search v-on:search="doSearch"/>
  <list 
    v-bind:anecdotes="filteredJokes"
  />
  </div>
</template>

<script>
import list from '@/components/list'
import search from '@/components/search'
export default {
  data() {
    return {
      anecdotes: [],
      temporarySearch: "",
    }
  },
  name: 'App',
  mounted() {
    fetch('https://v2.jokeapi.dev/joke/Programming?type=single&amount=10')
      .then(response => response.json())
      .then(json => {
        this.anecdotes = json.jokes.map((anec) => {anec.liked = JSON.parse(localStorage.getItem("joke_" + anec.id)); return anec})
      })
  },
  components: {
    list, search
  },
  computed: {
    filteredJokes() {
      return this.anecdotes.filter((a) => a.joke.toLowerCase().includes(this.temporarySearch.toLowerCase()));
    }
  },
  methods: {
    doSearch(searchVal) {
      this.temporarySearch = searchVal
    }
  },
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

pre {
  text-align: left;
}
</style>
