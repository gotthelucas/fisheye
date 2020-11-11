<template>
  <Botonera></Botonera>
</template>

<script>
import Botonera from './Botonera'

export default {
  name: 'Main',
  components: {
    Botonera
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
