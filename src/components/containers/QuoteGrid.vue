<template>
  <div class="quote-grid">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-sm-12 col-12" v-for="item in mocks" :key="item.id">
          <quote-block :quote="item" v-on:add-heart="onAddHeart($event, item)"></quote-block>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteBlock from '@/components/blocks/QuoteBlock'
import firestore from '../../firebaseInit.js'
  export default {
    name: 'quoteGrid',
    components: {
      QuoteBlock
    },
    created() {
      firestore.collection('quotes').get().then(querySnapshot => {
        querySnapshot.forEach(doc => {
          const data = {
            'id': doc.data().id,
            'content': doc.data().content,
            'hearts': doc.data().hearts,
            'author': doc.data().author,
            'contributor': doc.data().contributor,
            'socialUrl': doc.data().socialUrl
          }
          console.log(data)
          this.mocks.push(data)
        })
      })
    },
    data: function () {
      return {
        mocks: [],
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
      onAddHeart: function (event, quote) {
        quote.hearts += event
        firestore.collection('quotes').where('id', '==', quote.id).get()
          .then(querySnapshot => {
            querySnapshot.forEach(doc => {
              doc.ref.update({
                hearts: quote.hearts
              })
            })
          }).then(() => {
            console.log('success')
          })
          .catch(error => console.error(error))
      }
    }
  }
</script>