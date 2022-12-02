<template>
  <div class="subscribe">
    <div class="container">
      <div class="subscribe-wrapper">
        <div class="intro">
          <div class="intro-about">
            <div class="intro-about__btn">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M14 5l7 7m0 0l-7 7m7-7H3"
                />
              </svg>
            </div>
            <div class="intro-about__link">Meet your host</div>
            <div class="intro-about__name">Jacob Paulaner</div>
            <div class="intro-about__text">
              Jacob has a background in audio engineering, and has been
              podcasting since the early days.
            </div>
            <div class="intro-about__text">
              He’s here to help you level up your game by sharing everything
              he’s learned along the way.
            </div>
          </div>
          <div class="intro-image">
            <img src="../assets/img/Jacob.png" alt="" />
          </div>
        </div>
        <div class="subscribing">
          <div class="subscribing-about">
            <div class="subscribing-about__informing">Email Newsletter</div>
            <div class="subscribing-about__title">Subscribe for updates</div>
          </div>
          <div class="subscribing-inputs">
            <input type="text" class="subscribing-input__name" placeholder="Name">
            <input type="text" class="subscribing-input__email" placeholder="Email">
            <Button title="Submit" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from './Button.vue';
export default {
  components: { Button },
  name: "Subscribe",
};
</script>

<style lang="scss" scoped>
.subscribe {
  font-family: DM Sans;
  .intro {
    display: flex;
    align-items: center;
    @include breakpoint(lg){
      gap: 10px;
    }
    @include breakpoint(md){
      gap: 20px;
    }
    @include breakpoint(xs){
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &-image{
      img{
        @include breakpoint(lg){
          width: 500px;
        }
        @include breakpoint(md){
          width: 400px;
        }
        @include breakpoint(sm){
          width: 300px;
        }
        @include breakpoint(xs){
          width: 200px;
        }
      }
    }
    &-about {
      display: flex;
      flex-direction: column;
      gap: 20px;
      @include breakpoint(sm){
          gap: 10px;
      }
      &__btn {
        display: flex;
        justify-content: center;
        background-color: #00afd6;
        width: 112px;
        height: 112px;
        border-radius: 50%;
        @include breakpoint(md){
          width: 80px;
          height: 80px;
        }
        @include breakpoint(sm){
          width: 60px;
          height: 60px;
        }
      }
      &__link{
        font-size: 18px;
        line-height: 27px;
        color: #00afd6;
      }
      &__name{
        font-size: 65px;
        line-height: 79px;
        letter-spacing: 2.88px;
        @include breakpoint(lg){
          font-size: 54px;
          line-height: 64px;
          letter-spacing: 2px;
        }
        @include breakpoint(md){
          font-size: 42px;
          line-height: 52px;
          letter-spacing: 1px;
        }
        @include breakpoint(sm){
          font-size: 32px;
          line-height: 30px;
          letter-spacing: 1px;
        }
      }
      &__text{
        font-size: 22px;
        line-height: 33px;
        padding: 20px;
        @include breakpoint(md){
          font-size: 18px;
          line-height: 22px;
          letter-spacing: 1px;
        }
        @include breakpoint(md){
          font-size: 16px;
          line-height: 18px;
          letter-spacing: normal;
        }
        @include breakpoint(md){
          font-size: 16px;
          line-height: 18px;
          letter-spacing: normal;
        }
      }
    }
  }
  .subscribing{
    display: flex;
    justify-content: space-between;
    height: 387px;
    padding: 60px;
    background: #000;
    align-items: center;
    border-radius: 32px;
    margin-top: 100px;
    @include breakpoint(lg){
      padding: 40px;
      height: 300px;
    }
    @include breakpoint(xs){
      display: flex;
      flex-direction: column;
      gap: 20px;
      align-items: start;
      height: 400px;
      padding: 40px;
    }
    &-about{
      &__informing{
        font-size: 18px;
        line-height: 27px;
        color: #00afd6;
      }
      &__title{
        font-size: 72px;
        line-height: 79px;
        letter-spacing: 2.88px;
        max-width: 420px;
        @include breakpoint(lg){
          font-size: 54px;
          line-height: 64px;
          letter-spacing: 1px;
        }
        @include breakpoint(md){
          font-size: 38px;
          line-height: 50px;
          letter-spacing: normal;
        }
        @include breakpoint(md){
          font-size: 32px;
          line-height: 42px;
          letter-spacing: normal;
        }
      }
    }
    &-inputs{
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &-input{
      &__name{
        width: 500px;
        height: 60px;
        background-color: #191919;
        border: none;
        border-radius: 10px;
        padding: 10px;
        color: #fff;
        outline: none;
        &::placeholder{
          color: #fff;
        }
        @include breakpoint(lg){
          width: 400px;
        }
        @include breakpoint(md){
          width: 300px;
        }
        @include breakpoint(sm){
          width: 200px;
        }
        @include breakpoint(xs){
          width: 240px;
        }
        @media screen and (max-width: 364px){
          width: 200px;
        }
      }
      &__email{
        width: 500px;
        height: 60px;
        background-color: #191919;
        border: none;
        border-radius: 10px;
        padding: 10px;
        outline: none;
        color: #fff;
        &::placeholder{
          color: #fff;
        }
        @include breakpoint(lg){
          width: 400px;
        }
        @include breakpoint(md){
          width: 300px;
        }
        @include breakpoint(sm){
          width: 200px;
        }
        @include breakpoint(xs){
          width: 240px;
        }
        @media screen and (max-width: 364px){
          width: 200px;
        }
      }
    }
    .btn{
      width: 87px;
      height: 48px;
      padding: 0;
    }
  }
}
</style>