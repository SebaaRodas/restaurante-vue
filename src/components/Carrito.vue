<template>
    <div class="container">
    <br><br>
      <h4>Carrito de compras</h4>
      <table class="table">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">Producto</th>
            <th scope="col">Cantidad</th>
            <th scope="col">Acción</th>
            <th scope="col">Total</th>
          </tr>
        </thead>
        <tbody id="items">
            <ItemCarrito v-for="item in items" :key="item.id" :item="item" />
        </tbody>
        <tfoot>
          <tr id="footer">
            <th scope="row" colspan="5" v-if="Object.keys(items).length === 0">Carrito vacío - comience a comprar!</th>
            <FooterCarrito v-else />
          </tr>
        </tfoot>
      </table>
    </div>
</template>
<script>
import { computed } from 'vue';
import { useStore } from 'vuex';
import ItemCarrito from '@/components/ItemCarrito.vue'
import FooterCarrito from '@/components/FooterCarrito.vue'
export default {
    components: {
        ItemCarrito, FooterCarrito
    },
    setup(){
        const store = useStore()
        const items = computed(() => store.state.carrito)
        return {items}
    }
     

}
</script>
<style>
h4{
  text-align: center;
}
</style>