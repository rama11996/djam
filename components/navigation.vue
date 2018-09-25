<template lang="pug">
section
  .container
    .menu(:class="{open: open}" )
      .mask(@click="toggle()")
      ul.nav(:class="{open: open}" )     
          li(v-for="item in menuItems")
            a(href="") {{ item }}
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

@mixin full-screen
  position: fixed
  right: 0
  top: 0
  bottom: 0
  left: 0

section
  background-color: #FFF
  @include fixed-e
  z-index: 105
  width: 9rem
  @media (max-width: 1000px)
    width: 12rem
  .container
    @media(max-width: 1000px)
      display: flex
    .menu
      .nav
        @include reset
        position: fixed
        top: 25rem
        right: 0rem     
        transform: translateX(12rem) translateY(-3rem) rotate(90deg)
        display: flex
        // visibility: hidden
        // &.open
        //   visibility: visible
        @media (max-width:1000px)
          transform : none 
          display: block
          top: 7rem
          right: 2rem
          position: none
          visibility: hidden
          &.open
            visibility: visible
        li 
          a
            margin-right: $space
            @media(max-width:1000px)
              font-size: 1.525rem
              line-height: 3rem
section
  .container
    .menu
      .mask
        @mixin full-screen
        z-index: 104

section
  .hamburger
    display: none
    @media (max-width: 1000px)
      display: block
      height: 2.5rem
      position: fixed
      right: 1rem


</style>
