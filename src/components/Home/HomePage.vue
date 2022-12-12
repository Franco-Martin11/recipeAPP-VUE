<template>
  <section class="main-container">
    <Heading></Heading>
    <Figure></Figure>
  </section>
</template>

<script>
import Figure from './components/Figure.vue';
import Heading from './components/Heading.vue';

export default { components: { Heading, Figure } };
</script>

<style lang="scss" scoped>
@import '@/assets/main.scss';
.main-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  width: 100%;
  gap: 1rem;
  justify-items: center;
  @include md{
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  }
}
</style>