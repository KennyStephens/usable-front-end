<template>
<v-layout align-center>
  <v-flex xs8>
    <img src="../assets/usable_logo.svg" alt="">
  </v-flex>

  <v-flex xs4 class="text-xs-right">
    <span
      class="login title font-weight-thin"
      @click="dialog=true"
    >LOG IN</span>
    <span class="ml-2 mr-2 title font-weight-light">|</span>
    <span class="font-weight-bold title contact">CONTACT US</span>
    <v-dialog
      v-model="dialog"
      width="500"
    >

      

      <v-card>
        <v-card-title
          class="headline grey"
          primary-title
        >
          Log Into <span><img class="ml-2" src="../assets/usable_logo.svg" alt=""></span>
        </v-card-title>

        <v-card-text>
          <input type="text" placeholder="Email Address">
          <input type="text" placeholder="Password">
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="cyan"
            flat
            @click="dialog = false"
          >
            Log In
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

  </v-flex>
  
</v-layout>
</template>

<script>
export default {
  data() {
    return {
      dialog: false
    }
  }
}
</script>

<style scoped>
  .login, .contact {
    cursor: pointer;
  }
  
  .login:hover, .contact:hover {
    color: #00bcd4;
  }

  input {
    border: 1px solid white;
    border-radius: 20px;
    color: white;
    padding: 10px 20px;
    width: 100%;
    background: #455A64;
    margin: 10px 0px;
  }

  ::placeholder {
    color: #fff;
  }
</style>

