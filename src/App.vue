<template>
<h1 v-if="likes > 0">Likes You Have: {{ likes }}</h1>

<h1 v-else>Nothing to Count</h1>
<b-button variant="danger" v-on:click="like()">
Like
</b-button>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',
  data() {
    return {
      likes: 0,
    }
  },
  methods: {
    like() {
      this.likes++;
      alert('Thanks!')
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
