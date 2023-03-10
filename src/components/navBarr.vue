<template>
    <v-app id="inspire"> <!--espacio arriba-->
      <v-navigation-drawer v-model="drawer"> <!--espacio al lado-->
        <!-- <botNav></botNav> cuando un componente necesita contenido se hace asi para meterlo en la mitad -->
        <botNav/>
      </v-navigation-drawer>
  
      <v-app-bar>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
  
        <v-toolbar-title>Nav</v-toolbar-title>
      </v-app-bar>
  
      <v-main>
        <slot></slot>
      </v-main>
    </v-app>
</template>
<script>

import { defineComponent } from 'vue';
import botNav from './botNav.vue';

export default defineComponent({
  name:'navBar',

  data: () => ({
    drawer: false
  }),

  components:{
    botNav,
  }
})
  </script>