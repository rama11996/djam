<template lang="pug">
section
  .container
    .footer
      .main
        .mail
          h6 Write to us 
          a(href="#") arrroommalae.com
        .nav
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
      .aside
        .external
          .social
            h5 Follow us on instagram
            img(src="../assets/images/insta.png")
          .hostmaker
            img(src="../assets/images/google_.png")


</template>
<script>
export default {
  
}
</script>
<style lang="sass">
@import 'assets/styles/includes'
section
  padding: 5rem 2rem 2rem 3rem
  font-family: futura-pt,serif
  .footer
    @media(min-width: 1000px)
      display: flex
    .main
      flex: 6
      .mail
        margin-bottom: 5rem
        h6
          font-size: 1.25rem
        a 
          font-size: 2rem
          font-weight: 500
          color: black
      .nav
        ul
          font-size: 1.5rem
          @include reset
          @media(min-width: 1000px)
            display: flex
          li 
            margin-right: 0.5rem
            line-height: 3rem
section
  .footer
    margin-bottom: 3rem
    .aside
      flex: 4
      text-align: center
      .external
        line-height: 4rem
        @media(min-width: 1000px)
          @include stack-r
          margin-top: 7rem
          
        .social
          display: flex
          padding: 1rem
          margin-right: 1rem
          justify-content: center
          h5
            margin-top: .5rem
            margin-right: 1rem
          img
            width: 2rem
            height: 2rem
        .hostmaker
          position: relative
          top: 10px
          img
            width: 9rem
            
          
</style>
