<template>
  <v-app id="usable-home" dark>
    <v-container fluid>
      <!-- Navbar -->
      <usable-navbar />
      <!-- Main Section  -->
      <component :is="selectedComponent" @changeComponent="selectedComponent = $event"></component>
      <!-- Footer -->
      <usable-footer />
     
    </v-container>
  </v-app>
    

</template>

<script>
import UsableHome from './components/UsableHome'
import UsableNavbar from './components/UsableNavbar'
import UsableFooter from './components/UsableFooter'
import UsableForm from './components/UsableForm'

export default {
  name: 'App',
  components: {
    UsableHome,
    UsableNavbar,
    UsableFooter,
    UsableForm
  },
  data () {
    return {
      selectedComponent: 'UsableHome'
    }
  }
}
</script>

<style scoped>
  #usable-home {
    background-image: url('./assets/background.png');
    background-size: cover;
  }
</style>
