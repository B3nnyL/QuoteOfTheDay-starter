<template>
  <div class="hero-wrapper">
    <div class="fluid-container">
      <div class="row">
        <div class="hero__text col-8">
          <h1 class="hero__h1s">{{pageTitle}}</h1>
          <p class="hero__p">{{pageDescription}}</p>
        </div>
      </div>
      <div v-if="showCTA" class="hero--btn">
        <router-link class="btn primary-btn btn--cta" to="add">{{btnTitle}}</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hero',
  props: {
    pageTitle: String,
    pageDescription: String,
    btnTitle: String,
    showCTA: Boolean
  }
}
</script>

<style lang="scss" scoped>
  .hero__text{
    margin: 46px auto;
    p{
      margin-top: 19px;
    }
  }
</style>
