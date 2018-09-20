<template lang="pug">
div
  nuxt
  .copyrights
    p.content
      | &copy; 2018 All Rights Reserved&nbsp;
    ul.link
      li
        a(href="#") maker.com
      li
        a(href="#") terms
      li
        a(href="#") privacy
</template>

<style lang="sass" scoped>
@import 'assets/styles/includes'


.copyrights
  text-align: center
  @media (min-width: 1000px)
    @include flex
    justify-content: center
  .content
  .link
    @include reset
    @media (min-width: 1000px)
      @include flex
      justify-content: center
    li
      margin: 0.5rem
      @media (min-width: 1000px)
        &:after
          content: "\b7"
          display: inline-block
          padding: 0.5rem
      &:last-child
        &:after
          content: s""
</style>

