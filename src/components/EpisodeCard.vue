<template>
  <div class="card">
      <div class="card-wrapper">
        <div class="card-image">
          <img :src="post.imgUrl" alt="" />
        </div>
        <div class="card-episode">
          <div class="card-episode__type">{{post.type}}</div>
          <div class="card-episode__number">{{post.episode}}</div>
          <div class="card-episode__title">
            {{post.title}}
          </div>
          <div class="card-episode__text">
            {{post.text}}
          </div>
          <Button title="View Episode Details"/>
        </div>
      </div>
    </div>
</template>

<script>
import Button from './Button.vue';
export default {
  components: { Button },
  name: "EpisodeCard",
  props: {
    post: {
      type: Object,
      required : true
    }
  }
};
</script>

<style lang="scss" scoped>
.card{
  background-color: #000;
  border-radius: 32px;
  padding: 40px;

  &-wrapper{
    display: flex;
    gap: 30px;
    @include breakpoint(sm){
      display: flex;
      flex-direction: column;
    }
  }
  &-image{
    img{
      @include breakpoint(sm){
      width: 150px;
      }
    }
  }
  &-episode{
    &__type{
      display: flex;
      justify-content: center;
      font-family: DM Sans;
      font-size: 18px;
      line-height: 27px;
      background-color: #191919;
      border-radius: 6px;
      width: fit-content;
      padding: 0 16px;
      margin-bottom: 50px;
      @include breakpoint(md){
      margin-bottom: 30px;
      }
    }
    &__number{
      font-family: DM Sans;
      color: #118DA8;
      font-size: 17px;
      line-height: 27px;
    }
    &__title{
      font-family: DM Sans;
      font-size: 56px;
      line-height: 64px;
      letter-spacing: 2.5px;
      margin-bottom: 28px;
      @include breakpoint(lg){
       font-size: 42px;
       line-height: 48px;
       letter-spacing: 2px; 
      }
      @include breakpoint(md){
       font-size: 28px;
       line-height: 36px;
       letter-spacing: 1px; 
      }
    }
    &__text{
      max-width: 757px;
      font-size: 27px;
      font-family: DM Sans;
      margin-bottom: 15px;
      @include breakpoint(lg){
       font-size: 22px; 
      }
      @include breakpoint(md){
       font-size: 18px; 
      }
    }
  }
}
</style>