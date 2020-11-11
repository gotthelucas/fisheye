<template>
  <v-app-bar id="main_header" app 
      light
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
      scroll-target="#rtcontent"
      scroll-threshold="500"
      v-bind:style="{ height: headerHeight}"
      >
      <template  v-slot:img="{ props }">
        <v-img class="headImg"
          v-bind="props"
          v-bind:style="{ height: headerHeight }"
        ></v-img>
      </template>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn><v-spacer></v-spacer>
      <v-toolbar-title>{{contentScroll}}</v-toolbar-title>
      
  </v-app-bar>
</template>

<script>
export default {
  name: 'Header',
  props: {
    contentScroll:Number
  },
  watch: { 
    contentScroll: function(newVal, oldVal) {
      var percent = (newVal*100)/400;
      if(percent >= 100) percent = 100;
      var subtotal = 100 - percent;

      var total = (subtotal * 60)/100;
      
      this.headerHeight = total + 'vh';
      if(total < 8)
        this.headerHeight = 'inherit';
    }
  },
  data () {
    return {
      headerHeight:'60vh'  
    }
  }
}
</script>

<style scoped>
#main_header
{
  pointer-events: none;
}
</style>
