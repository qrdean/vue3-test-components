<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Search @searchEvent="searchMethod"/>
  <InputField label="New Field" v-model="name"></InputField>
  <Btn msg="Button"/>
  <!-- <BookItem :bookObject="bookObject"/> -->
  <BookList :bookObjects="bookObjects" />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Btn from './components/Btn.vue'
import InputField from './components/InputField.vue'
// import BookItem from './components/BookItem.vue'
import BookList from './components/BookList.vue'
import Search from './components/Search.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    InputField,
    // BookItem,
    BookList,
    Btn,
    Search
  },
  methods: {
    searchMethod(event) {
      console.log(event)
    }
  },
  data() {
    return {
      name: '',
      searchData: '',
      bookObjects: [
        {
          id: 1,
          title: 'test title',
          checkedIn: true,
          author: 'Author'
        },
        {
          id: 2,
          title: 'test title 2',
          checkedIn: false,
          author: 'Author 2'
        }
      ],
      bookObject: {
        title: 'test title',
        checkedIn: true,
        author: 'Author'
      }
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
</style>
