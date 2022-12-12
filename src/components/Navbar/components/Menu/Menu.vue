<template>
  <div class="">
    <button @click="calculatedClick()">
      {{ !this.state ? this.icons.hamburger : this.icons.close }}
    </button>
    <div class="modal" v-show="this.state === true">
      <links-container></links-container>
      <search-icon></search-icon>
    </div>
  </div>
</template>

<script>
import LinksContainer from "../Links/LinksContainer.vue";
import SearchIcon from "../Search/SearchIcon.vue";

export default {
  name: "Menu",
  components: { LinksContainer, SearchIcon },
  data() {
    return { state: null, icons: { hamburger: "☰", close: "🗙" } };
  },
  methods: {
    calculatedClick() {
      console.log(this.state);
      return this.state ? (this.state = false) : (this.state = true);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/main.scss";
.modal{
  position: absolute;
  right:0;
  top:0;
}
</style>