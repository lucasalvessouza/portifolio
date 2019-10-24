<template>
  <v-container fluid id="skills" class="grey darken-2">
    <v-layout text-center wrap mt-5 mb-5>
      <v-row justify="center">
        <v-col class="col-12">
          <h1 class="display-3 font-weight-bold mb-3 white--text">Skills</h1>
        </v-col>
        <v-flex class="col-12 col-md-8" mt-3>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-vuejs</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-node</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-js</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-python</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-html5</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-docker</v-icon>
          <v-icon size="80px" class="mr-5 mt-4" color="white">fab fa-git</v-icon>
        </v-flex>
      </v-row>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader',
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify',
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify',
      },
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer',
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/layout/pre-defined',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
};
</script>
