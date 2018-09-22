<template lang="pug">
section
  .container
    .hamburger(@click="toggle()", :class="{open: open}" )
      img(src="../assets/images/hamburger.png")
    .mask(@click="toggle()", :class="{open: open}" )
    .nav(:class="{open: open}" )
      ul
        li 
          a(href="#") HOME
        li 
          a(href="#") ABOUT
        li 
          a(href="#") WORK
        li 
          a(href="#") PROCESS
        li 
          a(href="#") PRICING
        li 
          a(href="#") TEAM
        li 
          a(href="#") BLOG
        li 
          a(href="#") CONTACT
</template>
<script>
export default {
  data(){
    return{
      open: false
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
  .container
    .hamburger
      
    .mask
    .nav
      visibility: hidden
      &.open
        visibility: visible
      ul
        @include reset


</style>
