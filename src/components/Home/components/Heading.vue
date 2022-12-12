<template>
<article class="article-container">
  <h1 class="title">Let´s Start Cooking With Popoular Recipes</h1>
  <p class="paragraph">Want to learn cook but confused how to start?
No need to worry again!</p>

<div class="btn-container">
  <button>Get Started</button>
  <button>Explore Menu</button>
</div>
</article>
</template>

<script>
export default {

}
</script>
<style lang="scss" scoped>
@import '@/assets/main.scss';

.article-container {
  .title{
    font-family: $fontHeading;
    font-weight: 700;
    font-size: 64px;
  }
}
.btn-container{
  display: flex;
  flex-wrap: wrap;
  gap: .5rem;
}

</style>