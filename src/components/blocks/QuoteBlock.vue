<template>
  <div class="quote">
    <div class="quote--header">
      <span class="quote__heart">
        💛 {{quote.hearts}}
      </span>
    </div>
    <div class="quote--body">
      <blockquote class="quote__p">
        {{quote.content}}
      </blockquote>
      <p v-if="quote.author" class="quote__author">
        - {{quote.author}}
      </p>
      <p v-else class="quote__author">
        - Someone on the day
      </p>
      <a v-if="quote.contributor" class="quote__contributor" :href="quote.socialUrl">
        ✍️ {{quote.contributor}}
      </a>
      <span v-else class="quote__contributor">
        ✍️ Anonymous
      </span>
    </div>
    <div class="quote--footer">
      <button class="btn btn-primary btn--action" @click="$emit('add-heart', 1)">I Heart It</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'quoteBlock',
  props: {
    quote: Object
  }
}
</script>


<style lang="scss" scoped>
  .quote{
    border: 2px black solid;
    padding: 10px 25px 35px 25px;
    margin: 45px;
    &--header{
      padding: 10px;
      min-height: 45px;
    }
    &__heart{
      float: right;
    }
    &--body{
      padding: 10px;
    }
    &__p, &__author,&__contributor{
      padding-bottom: 10px;
    }
    &--footer{
      padding: 10px;
      min-height: 60px;
    }
  }
</style>


