<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar/Navbar.vue";
</script>

<template>
  <div class="">
    <Navbar></Navbar>
    <RouterView />
  </div>
</template>

<style lang='scss' scoped>
@import "./assets/main.scss";
.bgPrueba {
  background-color: #ccc;
  .prueba {
    color: red;
    @include sm {
      color: violet;
    }
    @include md {
      color: blue;
    }
    @include lg {
      color: $mainGreen;
    }
  }
}
</style>
