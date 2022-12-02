<template>
  <div class="header">
    <div class="container">
      <div class="header-wrapper">
        <div class="header-image">
          <img src="../assets/img/Frame.png" alt="" />
        </div>
        <div class="header-about">
          <div class="header-about__title">
            Take your podcast to the next level
          </div>
          <div class="header-guid">
            <div class="header-guid__title">Listen on</div>
            <div class="header-guid__wrapper">
              <a href="" class="header-guid__link">
                <img src="../assets/img/Spotify.png" alt="" />
              </a>
              <a href="" class="header-guid__link">
                <img src="../assets/img/IMAGE1.png" alt="" />
              </a>
              <a href="" class="header-guid__link">
                <img src="../assets/img/IMAGE2.png" alt="" />
              </a>
              <a href="" class="header-guid__link">
                <img src="../assets/img/IMAGE3.png" alt="" />
              </a>
              <a href="" class="header-guid__link">
                <img src="../assets/img/IMAGE4.png" alt="" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
.header {
  margin-top: 40px;
  &-wrapper {
    display: flex;
    gap: 40px;
    @include breakpoint(xs) {
      display: flex;
      flex-direction: column;
    }
  }
  &-image {
    img {
      @include breakpoint(lg) {
        width: 400px;
      }
      @include breakpoint(md) {
        width: 400px;
      }
      @include breakpoint(sm) {
        width: 250px;
      }
    }
  }
  &-about {
    display: flex;
    flex-direction: column;
    gap: 74px;
    @include breakpoint(sm) {
      gap: 30px;
    }
    @include breakpoint(xs) {
      gap: 10px;
    }
    &__title {
      font-family: DM sans;
      font-size: 70px;
      line-height: 88px;
      @include breakpoint(md) {
        font-size: 56px;
      }
      @include breakpoint(sm) {
        font-size: 46px;
        line-height: 56px;
      }
      @include breakpoint(xs) {
        font-size: 32px;
        line-height: 42px;
      }
    }
  }
  &-guid {
    display: flex;
    flex-direction: column;
    gap: 16px;
    padding-left: 22px;
    @include breakpoint(sm) {
      padding-left: 0;
    }
    @include breakpoint(xs) {
      gap: 10px;
    }
    &__wrapper {
      display: flex;
      gap: 17px;
      @include breakpoint(xs) {
        gap: 10px;
      }
    }
    &__title {
      font-family: DM Sans;
      font-size: 15px;
      line-height: 24px;
    }
  }
}
</style>