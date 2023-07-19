<template>
  <div>
    <main-page></main-page>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import MainPage from './views/main-page.vue';

export default defineComponent({
    name:"App",
    components:{
      MainPage
    },
    setup () {
        

        return {}
    }
})
</script>

<style scoped>

</style>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
