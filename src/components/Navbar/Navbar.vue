<template>
  <div class="container">
    <Logo></Logo>
    holas
    <Menu></Menu>
  </div>
</template>

<script>
import LinksContainer from "./components/Links/LinksContainer.vue";
import Logo from "./components/Logo/Logo.vue";
import Menu from "./components/Menu/Menu.vue";
import SearchIcon from "./components/Search/SearchIcon.vue";

export default {
  components: { Logo, Menu, LinksContainer, SearchIcon },
};
</script>

<style lang="scss">
.container {
  display: flex;
  flex-direction: row;
}
</style>