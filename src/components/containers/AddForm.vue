<template>
  <div class="add-form-wrapper">
    <div class="container">
      <form @submit.prevent="formSubmit">
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <label>Tell us a line inspired you today at Levels Conf*</label>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <textarea class="form__textarea" type="text" v-model="draft.content" maxlength="140" placeholder="140 characters maximum input." required></textarea>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <label class="">Who said it</label>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <input class="form__input" type="text" v-model="draft.author">
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <label class="">Something about yourself</label>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <input class="form__input" type="text" v-model="draft.contributor">
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <label class="">A link to your social ego (starting with http or https)</label>
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <input class="form__input" type="text" v-model="draft.socialUrl">
          </div>
        </div>
        <div class="row">
          <div class="col-12 col-sm-12 col-md-8 mx-auto">
            <button type="submit" class="btn btn-primary btn--action">Submit</button>
          </div>
        </div>
      </form>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <pre>
            {{draft}}
          </pre>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddForm',
  data: function() {
    return {
      draft: {
        content: "",
        author: "",
        contributor: "",
        hearts: 0,
        socialUrl:"",
        id: Date.now()
      }
    }
  },
  methods: {
    formSubmit: function() {
      console.log(this.draft)
    }
  }
}
</script>



<style lang="scss" scoped>
  form {
    text-align: left;
    padding: 20px 45px 45px 45px;
    .row {
      padding-top: 10px;
    }
  }
  button {
    margin-top: 45px;
  }
  pre{
    line-height: 1.8;
  }
</style>