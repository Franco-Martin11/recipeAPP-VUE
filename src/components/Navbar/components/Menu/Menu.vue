<template>
  <div class="">
    <button class="menu-btn" @click="calculatedClick()">
      {{ !this.state ? this.icons.hamburger : this.icons.close }}
    </button>
    <div
      class="modal"
      v-if="this.state === true"
      @wheel.prevent
      @touchmove.prevent
      @scroll.prevent
    >
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
    return { state: false, icons: { hamburger: "☰", close: "🗙" } };
  },
  methods: {
    calculatedClick() {
      return this.state ? (this.state = false) : (this.state = true);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/main.scss";
.menu-btn {
  font-size: 1.5rem;
  border: none;
  background: none;
  padding: 0.5rem;
  z-index: 10;
  position: sticky;
}
.modal {
  display: grid;
  place-content: center;
  width: 100%;
  min-height: 100vh;
  background: rgba(0, 0, 0, 0.233);
  position: absolute;
  top: 0;
  right: 0;
  z-index: 1;
}
</style>