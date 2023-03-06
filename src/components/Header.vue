<template >
    <div>
        <nav>
            <router-link to="/">Home</router-link> |
            <!-- <router-link to="/pizzas">Pizzas</router-link> |
            <router-link to="/empanadas">Empanadas</router-link> |
            <router-link to="/hammburguesas">Hamburguesas</router-link> |
            <router-link to="/bebidas">Bebidas</router-link> | -->
            <router-link to="/about">Contacto</router-link>
        </nav>
    </div>
</template>
<script>
    export default {
    name: 'Header',
    props: {
        
    }
    }
</script>