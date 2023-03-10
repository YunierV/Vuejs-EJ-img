<template>
  <navBar>
    <div class="about">
    <h1>This is an about page</h1>
  </div>
  </navBar>
  
</template>
<script>

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
