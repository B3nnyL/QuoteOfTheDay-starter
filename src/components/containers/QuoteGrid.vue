<template>
  <div class="quote-grid">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-sm-12 col-12">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'quoteGrid',
    data: function () {
      return {
        quotes: [],
        quote: {
          id: 123,
          content: 'And if you gaze long into an abyss, the abyess will also gae into thee. ',
          hearts: 233,
          author: 'friderich nietsche',
          contributor: '@wlfp from Devhub',
          socialUrl: 'https://www.twitter.com/_wlfp'
        }
      }
    },
    methods: {
    }
  }
</script>