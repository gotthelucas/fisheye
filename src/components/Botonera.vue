<template>
  <v-container class="botonera">
      <v-row dense>
        <v-col cols="12">
          <v-card
            class="super_round"
            color="#385F73"
            dark
          >
            <v-card-title class="headline">
              Plan Base
            </v-card-title>
            <v-card-subtitle>
              Obtenes una aplicación progresiva para fidelizar a tus clientes, con una botonera de productos personalizada.
            </v-card-subtitle>

            <v-card-actions>
              
              <v-btn
                    class="ml-2 mt-5"
                    outlined
                    rounded
                    small
                  >
                    Contratar Ahora
                  </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card class="super_round"
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.artist"></v-card-subtitle>

                <v-card-actions>
                  <v-btn
                    v-if="item.artist === 'Cotización Customizada'"
                    class="ml-2 mt-3"
                    fab
                    icon
                    height="40px"
                    right
                    width="40px"
                  >
                    <v-icon>mdi-play</v-icon>
                  </v-btn>

                  <v-btn v-else text>
                    Cotizar
                   </v-btn>

                  


                </v-card-actions>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>

<script>
export default {
  name: 'Botonera',
  components: {
  },
  data () {
    return { 
      items: [
        {
          color: '#1F7087',
          src: 'https://www.qrcode-monkey.com/img/default-preview-qr.svg',
          title: 'Plan 2',
          artist: 'Realizá tu pedido de piezas gráficas',
        },
        {
          color: '#952175',
          src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
          title: 'Plan 3',
          artist: 'Cotización Customizada',
        },
      ],      
    }
  }
}

</script>

<style scoped>
 .super_round
 {
   border-radius: 20px;
 }

 .botonera
 {
   padding-bottom:60px;
 }
</style>
