<template>
  <div class="subtitle">
    <div class="container">
      <div class="subtitle-wrapper">
        <Review v-for="review in reviews" :key="review.autor" :review="review"/>
      </div>
    </div>
  </div>
</template>

<script>
import Review from './Review.vue'
export default {
  components: { Review },
  name: 'Subtitle',
  data () {
    return {
      reviews: [
        {
          comment: 'I can’t recommend this podcast enough',
          autor: 'Betty Lacey'
        },
        {
          comment: 'Jacob is the best in the business',
          autor: 'Adam Driver'
        },
        {
          comment: 'A wealth of audio knowledge',
          autor: 'Marcus Brown'
        },
        {
          comment: 'Every episode is a gem!',
          autor: 'Jessica Knowl'
        },
        {
          comment: 'Whoa whoa, let me take some notes!',
          autor: 'Scott Adams'
        },
        {
          comment: 'I’ve upped my game considerably since I started listening',
          autor: 'Steven Blast'
        }

      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.subtitle{
  margin: 100px 0;
  &-wrapper{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-self: center;
    gap: 10px;
    @include breakpoint(xs){
      grid-template-columns: 1fr 1fr;
    }
    @media screen and (max-width: 361px){
      gap: 5px;
    }
  }
}
</style>