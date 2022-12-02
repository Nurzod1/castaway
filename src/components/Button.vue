<template>
  <button class="btn">{{title}}</button>
</template>

<script>
export default {
  name: 'Button',
  props:{
    title:{
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.btn{
      padding: 10px 17px;
      background-color: #118DA8;
      border-radius: 10px;
      font-family: DM Sans;
      font-size: 17px;
      line-height: 27px;
      color: #fff;
      cursor: pointer;
      transition: 0.3s;
      &:hover{
        background-color: #00afd6;
      }
      @include breakpoint(sm){
        padding: 5px 10px;
      }
    }
</style>