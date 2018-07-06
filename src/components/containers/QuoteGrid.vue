<template>
  <div class="quote-grid">
    <div class="container">
      <div class="row">
        <div v-for="item in mocks"  v-bind:key="item.id" class="col-md-6 col-sm-12 col-12">
          <quote-block v-bind:quote="item" v-on:add-heart="onAddHeart($event, item)"></quote-block>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import quoteBlock from '@/components/blocks/QuoteBlock'
  export default {
    name: 'quoteGrid',
    components: {quoteBlock},
    data: function () {
      return {
        quote: {
          id: 123,
          content: 'And if you gaze long into an abyss, the abyess will also gae into thee. ',
          hearts: 233,
          author: 'friderich nietsche',
          contributor: '@wlfp',
          socialUrl: 'https://www.twitter.com/_wlfp'
        },
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
        }]
      }
    },
    methods: {
      onAddHeart: function (event, quote) {
        quote.hearts += event
      }
    }
  }
</script>