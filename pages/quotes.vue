<template>
  <div id="quotes">

      <h2 v-if="$cookie.get('language') == 'dutch'">Waarom ben je hier lid geworden?</h2>
      <h2 v-if="$cookie.get('language') == 'english'">Why did you become a member?</h2>

      <carousel class="carousel"
        :perPage="cardsamount"
        :paginationEnabled="false"
        :loop="true"
        :navigationEnabled="true"
        :navigationClickTargetSize="5"
        :paginationActiveColor="'#0d8141'"
        :navigationPrevLabel="' '"
        :navigationNextLabel="' '">
        <slide class="slide" v-for="(i, index) of quotes" :key="index">
          <div class="slide-container">
            <img class="photo" :src="`/quotes/${i.person}.jpg`">
            <p>"{{i.quote}}"</p>
            <i> - {{i.person}} </i>
          </div>
        </slide>
      </carousel>

    <div class="verenigingtriangles"></div>
  </div>
</template>

<script>
import quotes from '~/assets/quotes'

export default{
  data(){
    return{
      quotes: quotes.sort(function() {
        return .5 - Math.random();
      })
    }
  },

  computed: {
    cardsamount: function(){
      switch(this.$mq){
        case 'mobile':
          return 1
          break
        case 'twocards':
          return 2
          break
        case 'threecards':
          return 3
          break
        case 'fourcards':
          return 4
          break
        case 'fivecards':
          return 5
          break
        case 'desktop':
          return 5
          break
      }
    }
  }
}

</script>

<style>

#quotes{
  padding: 100px 0px;
  background-color: #f5eb22;
  color: white;
  position: relative;
  background-image: url('~/assets/fotos/bolk.jpg');
  background-size: cover;
  background-position: bottom;
}

#quotes h2{
  color: #0d8141 !important;
}

#quotes .VueCarousel-navigation button{
	margin-left: 20px;
	margin-right: 20px;
	border: solid #0d8141;
	border-width: 0 2px 2px 0 !important;
	width: 30px;
	height: 30px;
}

.VueCarousel-navigation-prev{
  transform: rotate(135deg) !important;
}

.VueCarousel-navigation-next{
  transform: rotate(-45deg) !important;
}

.carousel{
  margin-top: 20px;
	padding-left: 60px;
	padding-right: 60px;
}

.slide-container{
  font-weight: 500;
  border-radius: 10px;
  background-color: #0d8141;
  padding: 20px;
  margin: 0 10px;
  height: 100%;
}

.photo{
  border-radius: 10px;
  width: 100%;
  max-width: 150px;
  margin-left: auto;
  margin-right: auto;
  display: block;
  margin-bottom: 10px;
  border: 2px solid #f5eb22;
}

</style>
