<template>
  <v-app>
    <TopBar/>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>
<script>
import TopBar from './components/shared/TopBar.vue'

export default {
  name:'App',
  components: {
    TopBar
  }
}
</script>
<style>

</style>
