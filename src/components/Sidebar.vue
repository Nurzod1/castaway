<template>
  <div :class="['sidebar', { active: active }]">
    <div class="sidebar-wrapper">
      <div class="sidebar-logo">Castaway</div>
      <div class="sidebar-menu">
        <div class="sidebar-menu__link">Home</div>
        <div class="sidebar-menu__link">Episodes</div>
        <div class="sidebar-menu__link">About</div>
        <div class="sidebar-menu__link">Contact</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  props: {
    active: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.sidebar {
  display: flex;
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  width: 300px;
  background: #000;
  color: #fff;
  transform: translateX(-100%);
  transition: 0.3s;
  z-index: 1000;
  @media screen and (max-width: 381px){
      width: 250px;
    }
  &.active {
    transform: translateX(0);
  }
  &-wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 30px;
    padding-top: 20px;
    align-items: center;
    text-align: center;
  }
  &-logo {
    font-family: DM sans;
    font-size: 27px;
    font-weight: 700;
  }
  &-menu {
    display: flex;
    flex-direction: column;
    gap: 40px;
    @include breakpoint(sm) {
      gap: 20px;
    }
    @include breakpoint(xs) {
      gap: 10px;
    }
    &__link {
      font-family: DM sans;
      transition: 0.5s;
      &:hover {
        color: #118da8;
      }
    }
  }
}
</style>