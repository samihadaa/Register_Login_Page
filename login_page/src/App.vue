<template>
  <v-app>
    <v-app-bar app color="blue" dark>
      <v-toolbar-title>Login</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>
      <v-btn text rounded>About</v-btn>
      <v-btn text rounded>Contact Us</v-btn>
    </v-app-bar>
    <v-content>
      <v-card width="500" class="mx-auto mt-9">
        <v-card-title>Long Area</v-card-title>
        <v-card-text>
          <v-text-field label="Username" prepend-icon="mdi-account-circle"></v-text-field>
          <v-text-field label="Password"
          prepend-icon="mdi-lock" 
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword= !showPassword"
          :type="showPassword ? 'text':'password'"></v-text-field>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success" rounded>Register</v-btn>
          <v-btn color="info" rounded>Login</v-btn>
        </v-card-actions>
      </v-card>
    </v-content>

  <v-footer
    color="primary lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Welcome to Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>

  </v-app>
</template>

<script>
export default {
data(){
  return {
    showPassword: false,
  }
},
}
</script>

<style>

</style>