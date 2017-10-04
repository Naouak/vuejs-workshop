<template>
  <div id="app">
    <ol class="list">
      <li><Question></Question></li>
      <li><Question></Question></li>
      <li><Question></Question></li>
    </ol>

  </div>
</template>

<script>
import Question from './components/Question.vue';

export default {
  name: 'app',
  data () {
    return {}
  },
  components: {
  	Question
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: circle;
  padding: 0;
}

li {
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
