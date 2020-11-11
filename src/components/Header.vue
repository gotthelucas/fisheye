<template>
  <v-carousel vertical :show-arrows="false" show-arrows-on-hover hide-delimiter-background delimiter-icon="mdi-circle-small" :continuous="true"
      :cycle="false">
    <v-carousel-item>
        <v-parallax light src="static/img/journey.jpg">
        <v-row align="center" justify="center" >
          <v-col class="text-center"  cols="12">
            <h1 class="display-1 font-weight-thin mb-4">
              Fidelización
            </h1>
            <h4 class="subheading">
              Que tu cliente vuelva
            </h4>
          </v-col>
        </v-row>
        </v-parallax>
    </v-carousel-item>

    <v-carousel-item>
      <!--<video height="100%" autoplay loop>
        <source src="static/cty.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>--><!--ano anda en mobile el video-->
      <v-row align="center" justify="center" class="overvideo">
          <v-col class="text-center"  cols="12">
            <h1 class="display-1 font-weight-thin mb-4">
              Independencia
            </h1>
            <h4 class="subheading">
              Liberate de la playstore
            </h4>
          </v-col>
        </v-row>
    </v-carousel-item>
    
    <!--<v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>-->
  </v-carousel>
</template>


<script>
//import VideoParallax from 'vuetify-video-parallax';
  
  export default {
    components: {
     //VideoParallax
    },
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>

<style scoped>
#main_header
{
  pointer-events: none;
}

.overvideo
{
    position: absolute;
    top:0;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
    margin: 0;
    background-color: rgba(0,0,0,.5);
}
</style>
