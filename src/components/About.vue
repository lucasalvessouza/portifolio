<template>
  <v-container fluid id="about" class="grey darken-4">
    <v-layout text-center wrap mt-5>
      <v-flex mb-4 mt-5>
        <h1 class="display-3 font-weight-bold mb-3 white--text">Who am I?</h1>
      </v-flex>
      <v-row justify="center">
        <v-col class="col-8">
          <h5 class="headline mb-3 white--text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            Ut accumsan tortor at elit vestibulum, et finibus eros sodales.
            Etiam ac volutpat quam. Ut et arcu et tellus condimentum accumsan.
            Orci varius natoque penatibus et magnis dis parturient montes, nascetur
            ridiculus mus. Donec aliquam egestas neque, vitae egestas neque bibendum sit amet.
            Praesent faucibus orci et arcu facilisis, quis hendrerit nunc porta.
          </h5>
        </v-col>
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
