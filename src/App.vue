<template>
  <!-- <div class="container">
      <Carrito />
      <hr>
      <div class="row">
        <Card v-for="producto of productos" :key="producto.id" :producto="producto"/> 
      </div>
  </div> -->
  <router-view/>
</template>

<script>
import Header from '@/components/Header.vue';
// import Carrito from '@/components/Carrito.vue'
// import {useStore} from 'vuex'
// import { computed, onMounted } from 'vue'
// import Card from '@/components/Card.vue'


export default {
  name: 'App',
  components: {
    Header
    // Carrito,
    // Card
},
  // setup(){
  //   const store = useStore()
  //   //para usar el onMounted hay que importar y llamar al useStore() que también hay que importarlo
  //   onMounted(async() => {
  //     //dispatch dispara la acción
  //     store.dispatch('fetchData')
  //   })
  //   //el state se mapea mediante el computed 
  //   const productos = computed(() => store.state.productos)
  //   const carrito = computed(() => store.state.carrito)
  //   return {productos, carrito}
  // }
}
</script>

<style>
body{
  background-image: linear-gradient(to right top, #3fa391, #33958e, #2d8789, #2c7881, #2f6a77);
}
</style>
