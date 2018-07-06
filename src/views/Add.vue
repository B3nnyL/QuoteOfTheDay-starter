<template>
  <div class="add-wrapper">
    <hero
    pageTitle="Add A Quote"
    pageDescription="Share the moment you find inspiration"
    :showCTA="false"></hero>
   <add-form></add-form>
  </div>
</template>

<script>
import Hero from '@/components/containers/Hero'
import AddForm from '@/components/containers/AddForm'

export default {
  name: 'Add',
  components: {
    Hero,
    AddForm
  }
}
</script>

<style lang="scss" scoped>
  
</style>
