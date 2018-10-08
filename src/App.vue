<template>
  <v-app id="usable-home" dark>
    <v-container fluid>
      <v-layout align-center>
        <v-flex xs8>
          <img src="./assets/usable_logo.svg" alt="">
        </v-flex>
        <v-flex xs4>
          <h3 class="text-xs-right"><span class="subheading font-weight-thin">LOG IN</span><span class="pr-2 pl-2">|</span>CONTACT US</h3>
        </v-flex>
      </v-layout>

      <v-layout id="main-section" wrap align-content-center>
        <v-flex xs12>
          <h1 class="text-sm-center display-1">A testing platform to enhance your <span style="text-decoration: underline;">User's Experience</span></h1>
        </v-flex>

        <v-flex xs12 class="text-sm-center">
          <input class="mt-4" type="text" placeholder="Enter Site Link...">
          <v-btn class="d-block ma-auto mt-3 pl-5 pr-5" round color="cyan">CONTINUE<i class="ml-2 fas fa-chevron-right"></i></v-btn>
          <p class="pt-5">New to <span class=" font-italic font-weight-medium">usable</span>? <span style="text-decoration: underline;">Click Here</span> to learn how to use the platform!</p>
        </v-flex>

      </v-layout>
      
      <!-- Footer -->
      <v-footer fixed app>
      <span>Usable &copy; 2018</span>
      </v-footer>
    </v-container>
  </v-app>
    

</template>

<script>
import UsableHome from './components/UsableHome'

export default {
  name: 'App',
  components: {
    UsableHome
  },
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  #usable-home {
    background-image: url('./assets/background.png');
    background-size: cover;
  }

  #main-section {
    height: 100%;
  }

  input {
    border: 2px solid white;
    color: white;
    border-radius: 50px;
    padding: 10px 20px;
    width: 50%;
    background: #455A64;
  }
</style>
