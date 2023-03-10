<template>
  <NavBarr>
    <HelloWorld/>
  </NavBarr>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import HelloWorld from '../components/HelloWorld.vue';
import NavBarr from '../components/navBarr.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    HelloWorld,
    NavBarr,
  },
});
</script>
