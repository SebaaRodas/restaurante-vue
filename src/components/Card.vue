<template>
    <div class="col-12 col-sm-4 col-md-3 col-lg-2 mb-3">
        <div class="card">
            <img :src="producto.thumbnailUrl" alt="imagen-${ producto.title }" class="card-img-top" />
            <div class="card-body centrar">
                <h5 class="card-title ">{{ producto.title }}</h5>
                <p class="card-text ">${{ producto.precio }}</p>
                <button class="btn btn-dark" @click="agregar(producto)">Comprar</button>
            </div>
        </div>
      </div>
</template>
<script>
import { useStore } from 'vuex';

export default {
    name: 'Card',
    props: ['producto'],
    setup(){
        const store = useStore()
        const agregar = (producto) => {
            store.dispatch('agregarAlCarro', producto)
        }
        return {agregar}
    }
}
</script>
<style>
.centrar{
    text-align: center;
}
img{
    width: 200px;
    height: 150px;
}
@media screen and (max-width: 576px) {
    img{
        width: 150px;
        height: auto;
    }
}
</style>
