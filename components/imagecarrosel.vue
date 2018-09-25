<template lang="pug">
.imagecarrosel
  .title
    h1 What we Do
  ul.slides
    li(v-for="(img,i) in images", :class="{active: i === current}")
      img(:src="img.pic")
      h3 {{ img.name }}
  .pagination
    button.prev(@click="prev()") <
    button.next(@click="next()") >     
       
</template>
<script>
export default {
  data () {
    return {
      images: [
         { pic: '/images/images_1.jpg', name:'Blog1'},
         { pic: '/images/images_2.jpg', name:'Blog2'},
         { pic: '/images/images_3.jpg', name:'Blog3'},
         { pic: '/images/images_4.jpg', name:'Blog4'},
         { pic: '/images/images_5.jpg', name:'Blog5'}
      ],
      current: 0
    }
  },
   methods: {
    prev() {
      this.current= Math.abs((--this.current) % this.images.length)
    },
    next() {
      this.current= Math.abs((++this.current) % this.images.length)
    }
  }
}
</script>
<style lang="sass" scoped>
.imagecarrosel
  margin: 2rem
  ul
    li
      background-repeat: no-repeat
      list-style: none
      display: none
      margin-left: auto
      margin-right: auto
     
      &.active
        display: block
      img  
        height: 360px
      h3
        color: green 
  .pagination
    align-content: center        
</style>
