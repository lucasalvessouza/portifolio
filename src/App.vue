<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title>Lucas Alves</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="item in menu"
          :key="item.icon"
          :to="item.link"
          text
          @click="$vuetify.goTo(item.section)"
        >
          <span class="mr-2">
            {{
            item.title
            }}
          </span>
        </v-btn>
      </v-toolbar-items>
      <div class="d-lg-none"></div>

      <div class="d-lg-none">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      </div>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <v-list-item>
        <v-list-item-avatar>
          <v-img :src="require('./assets/lucas.jpg')"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Lucas Alves</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in menu"
          :key="item.title"
          link
          @click="$vuetify.goTo(item.section)"
        >
          <v-list-item-icon>
            <v-icon>mdi-{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <Main />
      <About />
      <Skills />
      <History />
    </v-content>
  </v-app>
</template>

<script>
import Main from './components/Main';
import About from './components/About';
import Skills from './components/Skills';
import History from './components/History';

export default {
  name: 'App',
  components: {
    Main,
    About,
    Skills,
    History
  },
  data: () => ({
    menu: [
      { icon: "home", title: "Home", section: "#home" },
      { icon: "information", title: "About", section: "#about" },
      { icon: "code-tags", title: "Skills", section: "#skills" },
      { icon: "code-rocket", title: "History", section: "#history" }
    ],
    drawer: false,

  }),
  methods: {
    menuItems() {
      return this.menu;
    }
  }
};
</script>
