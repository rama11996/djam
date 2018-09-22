<template lang="pug">
section
  .container
    
    .menu(:class="{open: open}" )
      .mask(@click="toggle()")
      .nav(:class="{open: open}" )
        .menu-item
          ul 
            li(v-for="item in menuItems") {{ item }}
    .hamburger(@click="toggle()", :class="{open: open}" )
      img(src="../assets/images/hamburger.png")
</template>
<script>
export default {
  data(){
    return{
      open: false,
      menuItems:['HOME','ABOUT','WORK','PROCESS','PRICING','TEAM','BLOG','CONTACT']
    }

  },
  methods:{
      toggle(){ 
         this.open = !this.open
    }
  }
}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
section
  position: fixed
  z-index: 105
  .container
    @media (max-width: 1000px)
      display: flex
      float: right
    .hamburger
      display: none
      @media (max-width: 1000px)
        display: block
        height: $space*2
        position: fixed
        right: 2rem
        z-index: 105
section
  .menu
    @media (max-width: 1000px)
      position: fixed
      right: 2rem
      z-index: 105  
      margin-top: 3rem
      line-height: $space*3
      font-size: $space*2 
      ul
        @include reset

      .nav
        visibility: hidden
        &.open
          visibility: visible
section
  .menu-item
    @media ( min-width:1001px)
      position: fixed
      top: 25rem
      right: 2rem
      z-index: 105  
      transform: translateX(12rem) translateY(-3rem) rotate(90deg)
    ul
      @media ( min-width:1001px)
        @include reset
        padding: 0
        display: flex
      li
        margin-right: $space

</style>
