<template>
  <v-app>
    <div class="outer">
      <div class="inner">
        <Nav></Nav>
        <router-view></router-view>
      </div>
    </div>
  </v-app>
</template>

<script>
import Nav from "./components/Nav.vue";
export default {
  name: 'App',
  components: {
    Nav
  },
  data () {
    return {
      //
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
*::-webkit-scrollbar {
  width: 0 !important;
}
</style>
