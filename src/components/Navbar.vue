<template>
  <div class="navbar">
    <div class="container">
      <div class="navbar-wrapper">
        <div class="navbar-logo">
          Castaway
        </div>
        <div class="navbar-menu">
          <div class="navbar-menu__link">Home</div>
          <div class="navbar-menu__link">Episodes</div>
          <div class="navbar-menu__link">About</div>
          <div class="navbar-menu__link">Contact</div>
        </div>
        <BurgerMenu :value="value" @input="$emit('input', $event)"/>
      </div>
    </div>
  </div>
</template>

<script>
import BurgerMenu from './BurgerMenu.vue'


export default {
  components: { BurgerMenu },
  name: 'Navbar',
  props: {
    value: {
      type: Boolean,
      required: true, 
    }
  },
}
</script>

<style lang="scss" scoped>
.navbar{
  &-wrapper{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &-logo{
    font-family: DM sans;
    font-size: 27px;
    font-weight: 700;
  }
  &-menu{
    display: flex;
    gap: 40px;
    @include breakpoint(sm){
      gap: 20px;
    }
    @include breakpoint(xs){
      gap: 10px;
    }
    @include breakpoint(sm){
      display: none;
    }
    &__link{
      font-family: DM sans;
      transition: 0.5s;
      cursor: pointer;
      &:hover{
        color: #118DA8;
      }
    }
  }
}
</style>