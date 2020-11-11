<template>
<v-app>
  <!--<v-navigation-drawer app>
    
  </v-navigation-drawer>-->
<v-system-bar class="head" height="30" lights-out light>
  <!--https://cdn.materialdesignicons.com/5.4.55/-->
  <!--<v-icon medium>mdi-chess-knight</v-icon> Holox-->
  <!--<v-icon medium>mdi-wind</v-icon> Bezier-->       
  <!-- <v-icon medium>mdi-fishbowl</v-icon>Fish-->
  <!--<v-icon medium>mdi-airballoon-outline</v-icon>Air Balloon-->
  <!--<v-icon medium>mdi-space-invaders</v-icon>Invasores-->
  <!--<v-icon medium>mdi-ocarina</v-icon>Ocarina-->
  <v-icon medium>mdi-panorama-fisheye</v-icon>Fisheye
  <!--<v-icon medium>mdi-jellyfish</v-icon>Jellyfish-->
  <v-spacer></v-spacer>
  Ecosistemas Virtuales
</v-system-bar>
  <Header :contentScroll="contentScroll" />

  <!-- Sizes your content based upon application components -->
  <v-main>
    <v-sheet>
      <v-container>
        <router-view ></router-view>
      </v-container>
    </v-sheet>
  </v-main>

  <v-footer
      absolute
      class="font-weight-medium"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Fisheye EV</strong>
      </v-col>
    </v-footer>
</v-app>
</template>

<script>
import Header from './components/Header'
export default {
  name: 'App',
  components:
  {
    Header
  },
  methods: {
    handleScroll (ev,el) {
      this.contentScroll = ev.srcElement.scrollTop;
    }
  },
  data () {
    return {
      contentScroll:0    
    }
  }
} 
</script>

<style>
.head
{
}
#app {
  font-family: 'Roboto','Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin: 0;
}
</style>