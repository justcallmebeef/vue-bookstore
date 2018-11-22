<template>
  <div id="app">
    <Search />
    <Card v-for="book in books" :key="book.id" :book="book"/>
  </div>
</template>

<script>
import Search from './components/Search.vue';
import Card from './components/Card.vue'
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

export default {
  name: 'app',
   data() {
    return {
      books: [],
    };
  },

  mounted() {
    axios.get("http://localhost:8082/api/books")
    .then(response => this.books = response.data)
  }, 
  components: {
    Search,
    Card
  }
}


</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
