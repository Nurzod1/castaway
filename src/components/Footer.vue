<template>
  <div class="footer">
    <div class="container">
      <div class="footer-wrapper">
        <div class="footer-contacts">
          <div class="footer-contacts__logo">Castaway</div>
          <div class="footer-contacts__links">
            <div class="footer-contacts__link">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M17 2H7C4.23858 2 2 4.23858 2 7V17C2 19.7614 4.23858 22 7 22H17C19.7614 22 22 19.7614 22 17V7C22 4.23858 19.7614 2 17 2Z"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M16 11.3698C16.1234 12.202 15.9812 13.052 15.5937 13.7988C15.2062 14.5456 14.5931 15.1512 13.8416 15.5295C13.0901 15.9077 12.2384 16.0394 11.4077 15.9057C10.5771 15.7721 9.80971 15.3799 9.21479 14.785C8.61987 14.19 8.22768 13.4227 8.09402 12.592C7.96035 11.7613 8.09202 10.9097 8.47028 10.1582C8.84854 9.40667 9.45414 8.79356 10.2009 8.40606C10.9477 8.01856 11.7977 7.8764 12.63 7.99982C13.4789 8.1257 14.2648 8.52128 14.8716 9.12812C15.4785 9.73497 15.8741 10.5209 16 11.3698Z"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M17.5 6.5H17.51"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
            <div class="footer-contacts__link">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M23 2.9998C22.0424 3.67528 20.9821 4.19191 19.86 4.52981C19.2577 3.83732 18.4573 3.3465 17.567 3.12373C16.6767 2.90097 15.7395 2.957 14.8821 3.28426C14.0247 3.61152 13.2884 4.19421 12.773 4.95352C12.2575 5.71284 11.9877 6.61214 12 7.5298V8.52979C10.2426 8.57536 8.50127 8.18562 6.93101 7.39525C5.36074 6.60488 4.01032 5.43844 3 3.9998C3 3.9998 -1 12.9998 8 16.9998C5.94053 18.3978 3.48716 19.0987 1 18.9998C10 23.9998 21 18.9998 21 7.49979C21 7.21979 20.97 6.93981 20.92 6.66981C21.9406 5.6633 22.6608 4.39252 23 2.9998Z"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
            <div class="footer-contacts__link">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M18 2H15C13.6739 2 12.4021 2.52678 11.4645 3.46447C10.5268 4.40215 10 5.67392 10 7V10H7V14H10V22H14V14H17L18 10H14V7C14 6.73478 14.1054 6.48043 14.2929 6.29289C14.4804 6.10536 14.7348 6 15 6H18V2Z"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="footer-menu">
          <div class="footer-menu__links">
            <div class="footer-menu__link">Home</div>
            <div class="footer-menu__link">About</div>
            <div class="footer-menu__link">Episodes</div>
            <div class="footer-menu__link">Contact</div>
          </div>
          <div class="footer-menu__links">
            <div class="footer-menu__link">Style Guide</div>
            <div class="footer-menu__link">Instructions</div>
            <div class="footer-menu__link">Changelog</div>
            <div class="footer-menu__link">Credit</div>
            <div class="footer-menu__link">Powered by Webflow</div>
            <div class="footer-menu__link">Licenses</div>
          </div>
        </div>
        <div class="footer-guid__wrapper">
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
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.footer {
  font-family: DM Sans;
  padding-bottom: 100px;
  @include breakpoint(md){
    padding-bottom: 50px;
  }
  &-wrapper{
    display: flex;
    @include breakpoint(md){
      display: flex;
      justify-content: space-between;
    }
    @include breakpoint(sm){
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }
    @include breakpoint(xs){
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    }
  }
  &-contacts {
    display: flex;
    flex-direction: column;
    gap: 20px;
    width: 447px;
    &__logo {
      font-family: DM sans;
      font-size: 27px;
      font-weight: 700;
    }
    &__links{
      display: flex;
      gap: 10px;
    }
    @include breakpoint(lg){
      width: 347px;
    }
    @include breakpoint(lg){
      width: 247px;
    }
    @include breakpoint(md){
      width: 200px;
    }
    @include breakpoint(xs){
      width: fit-content;
      align-items: center;
    }
  }
  &-menu{
    display: flex;
    gap: 120px;
      @include breakpoint(md){
        gap: 30px;
      }
      @media screen and (max-width: 361px){
      display: flex;
      flex-direction: column;
      text-align: center;
      gap: 30px;
    }
    &__links{
      display: flex;
      flex-direction: column;
      gap: 10px;  
    }
    &__link{
      cursor: pointer;
      transition: 0.3s;
      &:hover{
        color: rgba(255, 255, 255, 0.418);
      }
    }
  }
  &-guid{
    display: flex;
    flex-direction: column;
    gap: 16px;
    padding-left: 22px;
    &__wrapper{
      display: flex;
      gap: 17px;
      @include breakpoint(md){
        gap: 5px;
      }
    }
    &__title{
      font-family: DM Sans;
      font-size: 15px;
      line-height: 24px;
    }
  }

  svg {
    cursor: pointer;
    path {
      transition: 0.3s;
    }
  }
  svg:hover {
    path {
      stroke: rgba(255, 255, 255, 0.313);
    }
  }
}
</style>