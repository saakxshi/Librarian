<template>
  <v-app>
      <v-app-bar app color="primary" dark>
          <div class="d-flex align-center">
              <v-img alt="Vuetify Logo" class="shrink mr-2" contain src="@/assets/logo.png" transition="scale-transition" width="40" />
  
              <p>{{ $const.APP_NAME}}</p>
          </div>
  
          <v-spacer></v-spacer>
  
          <v-btn text>
              Login
          </v-btn>
          <v-btn text>
              <v-icon>mdi-account-circle</v-icon>
          </v-btn>
      </v-app-bar>
  
      <v-main>
          <router-view />
      </v-main>
  </v-app>
  </template>
  
  <script>
  export default {
      name: 'App',
  
      data: () => ({
          //
      }),
  };
  </script>
  
  <style>
  @import url('@/assets/styles.css');
  </style>
  