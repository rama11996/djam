<template lang="pug">
  .process
    .title
      h1 Process
    .summary
      p Morbi convallis ligula at molestie tempus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas
    .processes
      .step
        img(src="@/assets/images/process_1.png")
        p Site Inspection
      .step
        img(src="@/assets/images/process_2.png")
        p Initial Quote and Moodboard
      .step
        img(src="@/assets/images/process_3.png")
        p Design Presentation and Detailed Budget
      .step
        img(src="@/assets/images/process_4.png")
        p Buying, Storage Management and Installation
      .step
        img(src="@/assets/images/process_5.png")
        p Styling and Professional Photography
    .image   
      img(src="@/assets/images/process.png")  
</template>
<script>
export default {

}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
.process
  position: relative
  margin: 3rem
  .summary
    width: 100%  
    font-size: 1.7rem
    line-height: 30px
    font-weight: 200 
    @media (min-width: 900px)
      width: 40rem
  .processes
    margin-top: 5rem
    @media (max-width: 900px)
      padding-bottom: 400px
    .step
      img
        width: 2rem
        height: 2rem
      p
        margin-left: 0.5rem
        font-size: 1.3rem
        line-height: 30px
        font-weight: 200  
        
      @media (max-width: 900px)
        align-items: center
        display: flex
        flex-direction: column
        text-align: center
        p
          font-size: 1.3rem
      padding: 1rem
      display: flex 
      @media (min-width: 900px)
        margin-left: 45%       
          
  .image
  
    @media (max-width: 900px)
      @include absolute-s
    @media (min-width: 900px)
      @include absolute-sw      
</style>

