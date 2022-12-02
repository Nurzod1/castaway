<template>
  <div class="episodes">
    <div class="container">
      <div class="episodes-wrapper">
        <div class="episodes-intro">
          <div class="episodes-intro__title">Latest episodes</div>
          <Button title="View all episodes"/>
        </div>
        <EpisodeCard v-for="item in items" :key="item.imgUrl" :post="item"/>
      </div>
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'
import EpisodeCard from './EpisodeCard.vue'
export default {
  components: { EpisodeCard, Button },
  name: 'Episodes',
  data () {
    return {
      items: [
        {
          imgUrl: require('../assets/img/CardImg1.png'),
          type: 'Gear',
          episode: 'Episode 3',
          title: 'Should you get outboard audio gear?',
          text: 'Is hardware really worth it when it comes to podcasting? The answer is...it depends. Here’s our reasons on why you might want to consider picking something up.'
        },
        {
          imgUrl: require('../assets/img/Frame2.png'),
          type: 'Tips & Tricks',
          episode: 'Episode 2',
          title: 'Mic tricks to take you to the next level',
          text: 'Stop rolling with those default settings on your mic. These small tweaks will take you from sounding good to great.'
        },
        {
          imgUrl: require('../assets/img/Frame3.png'),
          type: 'Gear',
          episode: 'Episode 1',
          title: 'The best microphone under $200',
          text: 'With so many microphones on the market, how are you supposed to know what’s the best? Take a look at our top picks.'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.episodes{
  padding: 100px 0;
  @include breakpoint(md){
    padding: 50px 0;    
  }
  
  &-wrapper{
    display: flex;
    flex-direction: column;
    gap: 50px;
    @include breakpoint(md){
        gap: 25px;
      }
  }
  &-intro{
    display: flex;
    justify-content: space-between;
    align-items: center;
    @include breakpoint(xs){
        display: flex;
        flex-direction: column;
        align-items: start;
        gap: 10px;
        padding-left: 20px;
      }

    &__title{
      font-size: 64px;
      line-height: 79px;
      letter-spacing: 3px;
      font-family: DM Sans;
      @include breakpoint(md){
        font-size: 46px;
        line-height: 58px;
        letter-spacing: 1.5px;
      }
      @include breakpoint(sm){
        font-size: 24px;
        line-height: 34px;
        letter-spacing: 1px;
      }
    }
  }
}
</style>