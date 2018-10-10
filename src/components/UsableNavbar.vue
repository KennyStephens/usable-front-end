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
      width="600"
    >

      

      <v-card>
        <v-card-title
          class="headline grey justify-center"
          primary-title
        >
          Log Into <span><img class="ml-2" src="../assets/usable_logo.svg" alt=""></span>
        </v-card-title>

        <v-card-text>
          <input type="text" placeholder="Email Address">
          <input type="text" placeholder="Password">
          <v-layout row>
            <v-flex xs6>
                       <v-checkbox
            class="pl-2"
            v-model="checkbox"
            :error-messages="checkboxErrors"
            label="Remember Me"
            required
            @change="$v.checkbox.$touch()"
            @blur="$v.checkbox.$touch()"
          ></v-checkbox>
            </v-flex>
            <v-flex class="d-flex text-xs-right pr-2" xs6 align-center>
              <span class="forgot">Forgot Password</span>
            </v-flex>
          </v-layout>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions class="d-block text-xs-center">
          <v-spacer></v-spacer>
          <v-btn
            style="border-radius: 20px;"
            class="pr-5 pl-5 mt-3"
            color="cyan"
            @click="dialog = false"
          >
            Log In
          </v-btn>
          <p class="mt-3 mb-3">or</p>
          <v-btn
          style="border-radius: 20px;"
          class="pr-5 pl-5 mb-3"
          color="grey"
          >
          CREATE NEW ACCOUNT
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
  
  .login:hover, .contact:hover, .forgot:hover {
    color: #00bcd4;
    cursor: pointer;
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

