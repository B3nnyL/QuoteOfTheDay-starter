<template>
  <div class="home">
    <hero 
      pageTitle="A Mindfullness Page"
      pageDescription="Here, we collect inspirational quotes from talks and coversations during Levels Confs, which are contributed by you and your peers."
      btnTitle="Add a new quote"
      :showCTA="true"
    ></hero>

  </div>
</template>

<script>
// @ is an alias to /src
import Hero from '@/components/containers/Hero.vue'

export default {
  name: 'home',
  components: {
    Hero
  }
}
</script>
