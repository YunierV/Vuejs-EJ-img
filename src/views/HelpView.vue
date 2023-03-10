<!-- vista la cual hay que importar en el index de router, no hay que importar con comando aca solo en el index. -->
<template>
    <!-- html -->
    <navBar>
        <div>
            <h1>hola desde help</h1>
        </div>
    </navBar>
    
</template>
<script>
//comandos JS
import { defineComponent } from 'vue'; 
import navBar from '../components/navBarr.vue'
//creamos un objecto components que contenga el nombre de lo que estoy importando
export default defineComponent({
    name:'helpV',
    components:{
        navBar,
    }
})
</script>
<style>
/* estilos del CSS */

</style>