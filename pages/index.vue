<template>
  <div>
    <navbar></navbar>
    <imageheader></imageheader>
    <maintext></maintext>
    <vereniging></vereniging>
    <schema></schema>
    <kmt></kmt>
    <sleepin></sleepin>
    <quotes></quotes>
    <contact></contact>
    <sponsor></sponsor>
  </div>
</template>

<script>
  import imageheader from '~/pages/imageheader.vue'
  import quotes from '~/pages/quotes.vue'
  import vereniging from '~/pages/vereniging.vue'
  import maintext from '~/pages/maintext.vue'
  import schema from '~/pages/schema.vue'
  import kmt from '~/pages/kmt.vue'
  import sleepin from '~/pages/sleepin.vue'
  import contact from '~/pages/contact.vue'
  import navbar from '~/pages/navbar.vue'
  import sponsor from "~/pages/sponsor.vue";

  export default {
    components: {
      imageheader,
      quotes,
      vereniging,
      schema,
      maintext,
      kmt,
      sleepin,
      contact,
      navbar,
      sponsor
    },

    beforeCreate(){
      //set cookie if none
      if(this.$cookie.get('language') != 'dutch' && this.$cookie.get('language') != 'english'){
        this.$cookie.set('language', 'dutch', '100')
      }
    }
  }
</script>

<style>

body{
  margin: none;
  font-family: 'Montserrat', sans-serif !important;
  font-weight: 500;
}

html{
  font-size: 16px;
}

@font-face {
  font-family: 'Komikax';
  src: url('/fonts/KOMIKAX_.TTF') format('truetype')
}

h1, h2{
  text-align: center;
  color: white !important;
  font-family: 'Komikax', cursive;
  font-size: 3rem !important;
}

p{
  font-size: 1rem;
}

.content{
  max-width: 960px;
  margin: 0 auto;
  padding: 0 29px;
}

</style>
