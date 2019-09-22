<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>{</span>
        <span class="font-weight-light">LUCAS ALVES</span>
        <span>}</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text @click="$vuetify.goTo('#about',options)">
        <span class="mr-2">ABOUT</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">CONTACT</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Main />
      <About />
    </v-content>
  </v-app>
</template>

<script>
import Main from './components/Main';
import About from './components/About';

export default {
  name: 'App',
  components: {
    Main,
    About
  },
  data: () => ({
    //
  }),
};
</script>
