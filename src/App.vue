<template>
  <div id="app">
    <Header />
    <GalleryArea />
    <h1 v-bind:title="message">{{message}}</h1>
    <button v-on:click="reverseMessage">Reverse Message</button>
    <span v-if="seen">Visible</span>
    <ol>
      <TodoItem v-bind:todos="todos" />
      <!-- <li v-for="todo in todos" v-bind:key="todo.text">{{todo.text}}</li> -->
    </ol>
    <input type="text" v-model="message">
    <Lorem />
  </div>
</template>

<script>
  import Header from '@/components/Header';
  import GalleryArea from '@/components/GalleryArea';
  import Lorem from '@/components/LoremIpsum';
  import TodoItem from '@/components/TodoItem';

  export default {
    components: {
      Header,
      GalleryArea,
      Lorem,
      TodoItem
    },
    data() {
      return {
        message: 'Hello World!',
        seen: true,
        todos: [
          {text: 'Learn JavaScript'},
          {text: 'Learn Vue'},
          {text: 'Build something awesome'},
          {text: 'New item'}
        ]
      }
    },
    methods: {
      reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
      }
    }
  };
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
