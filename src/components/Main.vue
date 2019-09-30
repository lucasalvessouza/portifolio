<template>
  <v-container fluid style="height: 100%" id="home" class="grey lighten-3">
    <v-layout text-center wrap mt-5>
      <v-flex xs12 mb-5>
        <v-avatar size="300">
          <v-img :src="require('../assets/lucas.jpg')"></v-img>
        </v-avatar>
      </v-flex>

      <v-flex mb-4 mt-5>
        <h1 class="display-2 font-weight-thin mb-3">Developer</h1>
        <h2>Turning code into reality</h2>
      </v-flex>
    </v-layout>

    <v-layout text-center wrap>
      <v-container>
        <v-row>
          <v-col>
            <v-btn
              class="mx-8"
              icon
              v-for="item in social"
              :key="item.icon"
              :href="item.href"
              target="_blank"
            >
              <v-icon size="50px">{{ item.icon }}</v-icon>
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    social: [
      {
        href: 'https://www.linkedin.com/in/lucas-alves-s/',
        icon: 'fab fa-linkedin',
      },
      {
        href: 'https://github.com/lucasalvessouza',
        icon: 'fab fa-github',
      }
    ]
  }),
};
</script>
