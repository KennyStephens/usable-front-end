<template>
    <v-layout id="main-section" wrap align-content-center>
      <v-flex xs12>
        <h1 class="text-sm-center display-1">A testing platform to enhance your <span style="text-decoration: underline;">User's Experience</span></h1>
      </v-flex>

      <v-flex xs12 class="text-sm-center">
        <input class="mt-4" type="text" placeholder="Enter Site Link...">
        <v-btn class="d-block ma-auto mt-3 pl-5 pr-5" round color="cyan" @click="selectedComponent = 'UsableForm'">CONTINUE<i class="ml-2 fas fa-chevron-right"></i></v-btn>
        <p class="pt-5">New to <span class=" font-italic font-weight-medium">usable</span>? <span style="text-decoration: underline;">Click Here</span> to learn how to use the platform!</p>
      </v-flex>
    </v-layout>
</template>

<script>

</script>

<style scoped>
  #main-section {
    height: 100%;
  }

  input {
    border: 2px solid white;
    border-radius: 50px;
    padding: 10px 20px;
    width: 50%;
    background: #455A64;
  }
</style>
