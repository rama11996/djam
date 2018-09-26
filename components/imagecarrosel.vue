<template lang="pug">
.imagecarrosel
  .title
    h1 What we Do
  ul.slides
    li(v-for="(img,i) in images", :class="{active: i === current}")
      img(:src="img.pic")
      .content
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
      position: relative
      max-width: 500px
      list-style: none
      display: none
      margin: 0 auto
      &.active
        display: block
      img   
        width: 700px
      .content
        position: absolute
        bottom: 0
        height: 0
        background: rgb(0, 0, 0)
        background: #fff
        width: 100%
        padding: 5px
        transition: .5 s ease
        overflow: hidden
      &:hover
        .content  
          height: 30%
  .pagination 
    display: flex
    margin: 0 auto
    width: 100%
    justify-content: space-around
    .prev, .next
      padding: 20px
      border-radius: 3rem 
      // background: none
      color:grey
      // font-size: 2.5rem
      cursor: pointer          
</style>
