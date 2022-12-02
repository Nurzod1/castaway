<template>
  <div class="review">
    <div class="review-grade">
      <div class="review-grade__img">
        <img src="../assets/img/star.svg" alt="">
      </div>
      <div class="review-grade__img">
        <img src="../assets/img/star.svg" alt="">
      </div>
      <div class="review-grade__img">
        <img src="../assets/img/star.svg" alt="">
      </div>
      <div class="review-grade__img">
        <img src="../assets/img/star.svg" alt="">
      </div>
      <div class="review-grade__img">
        <img src="../assets/img/star.svg" alt="">
      </div>
    </div>
    <div class="review-comment">{{review.comment}}</div>
    <div class="review-autor">{{review.autor}}</div>
  </div>
</template>

<script>
export default {
  name: 'Review',
  props: {
    review: {
      type: Object,
      required : true
    }
  }
}
</script>

<style lang="scss" scoped>
.review{
  display: flex;
  flex-direction: column;
  gap: 20px;
  background-color: #000;
  font-family: DM Sans;
  padding: 50px;
  max-width: 373px;
  border-radius: 32px;
  @include breakpoint(sm){
    padding: 20px;
  }
  &-grade{
    display: flex;
    gap: 5px;
    @media screen and (max-width: 361px){
      gap: 0px;
    }
    img{
      @media screen and (max-width: 361px){
      width: 70%;
      height: 70%;
    }
    }
  }
  &-comment{
    font-size: 32px;
    line-height: 37px;
    @include breakpoint(md){
      font-size: 26px;
      line-height: 31px;
    }
    @include breakpoint(sm){
      font-size: 18px;
      line-height: 22px;
    }
    @media screen and (max-width: 361px){
      font-size: 16px;
      line-height: 18px;
    }
  }
  &-autor{
    font-size: 20px;
    line-height: 24px;
    
    @include breakpoint(md){
      font-size: 16px;
      line-height: 18px;
    }
    @media screen and (max-width: 361px){
      font-size: 14px;
      line-height: 16px;
    }
  }
}

</style>