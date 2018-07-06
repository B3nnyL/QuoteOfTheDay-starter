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
        mocks: [{
          id: 123,
          content: 'And if you gaze long into an abyss, the abyess will also gae into thee. ',
          hearts: 233,
          author: 'friderich nietsche',
          contributor: '@wlfp',
          socialUrl: 'https://www.twitter.com/_wlfp'
        },
        {
          id: 456,
          content: 'Knowledge is the most democratic source of power. ',
          hearts: 777,
          author: 'Alvin Toffler',
          contributor: '@wlfp',
          socialUrl: 'https://www.twitter.com/_wlfp'
        }],
        quote: {
          id: 123,
          content: 'And if you gaze long into an abyss, the abyess will also gae into thee. ',
          hearts: 233,
          author: 'friderich nietsche',
          contributor: '@wlfp',
          socialUrl: 'https://www.twitter.com/_wlfp'
        }
      }
    },
    methods: {
    }
  }
</script>