<template lang="pug">
.textcarrosel
  .image    
    img(src="../assets/images/teapoy.png")
  ul.slides
    li(v-for="(txt, i) in text", :class="{active: i === current}")
      p  {{ txt.quotes }}
      h2 {{ txt.author }}    
  .pagination
    button.prev(@click="prev()") <
    button.next(@click="next()") >    
</template>
<script>
export default {
  data() {
    return {
       text: [
         { author: 'Dale Carnegie', quotes: 'It isn\'t what you have or who you are or where you are or what you are doing that makes you happy or unhappy. It is what you think about it' },
         { author: 'Roy T. Bennett', quotes: 'Attitude is a choice. Happiness is a choice. Optimism is a choice. Kindness is a choice. Giving is a choice. Respect is a choice. Whatever choice you make makes you. Choose wisely.' },
         { author: 'Marcus Aurelius', quotes: 'If you are distressed by anything external, the pain is not due to the thing itself, but to your estimate of it; and this you have the power to revoke at any moment' },
         { author: 'Roy T. Bennett', quotes: 'You cannot control what happens to you, but you can control the way you think about all the events. You always have a choice. You can choose to face them with a positive mental attitude.' },
         { author: ' Dr Roopleen', quotes: 'If you have a dream, don’t just sit there. Gather courage to believe that you can succeed and leave no stone unturned to make it a reality.' }
       ],
       current: 0
    }
  },
  methods: {
    prev() {
      this.current= Math.abs((--this.current) % this.text.length)
    },
    next() {
      this.current= Math.abs((++this.current) % this.text.length)
    }
  }   
}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
$space: 3rem
.textcarrosel
  display: flex
  margin: 2rem
  .slides
    list-style: none
    li 
      height: 0rem
      visibility: hidden
      &.active
        visibility: visible  
  .pagination  
    .prev, .next
      padding: 20px
      border-radius: 2rem 
      font-size: 1.5rem
      cursor: pointer    
  .image
    width: 300px
    height: 300px
    // @media (max-width: 900px)
    //   @include absolute-sw
</style>
