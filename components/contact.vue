<template lang="pug">
.contact
  .content
    .titles
      h1 Contact
    .para
      p And let's get the design ball rolling!
      p Drop us a line with any enquiries or if you already have a project in mind. We will happily get back to you shortly
  .contact-form
    .name
      .firstname
        label First Name
        input(type="text")
      .lastname
        label Last name
        input(type="text")
    .email
      label E-mail
      input(type="email")
    .number
      label Mobile number
      input(type="tel")
    .textarea 
      label  Your Message      
      textarea 
</template>
<script>
export default {
  
}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
.contact
  display: flex
  max-width: 1350px
  height: 800px
  background-color: #f9f7f3
  .content, .contact-form
    margin-top: 5rem
   
  .contact-form
    width: 60%
    margin-right: 1rem
    input, label
      width: 100%
    .textarea
      textarea
        vertical-align: top  
    .name
      display: flex
      > div
        flex: 1
    input, textarea
      margin-right: 1rem
      box-sizing: border-box
    
    
</style>


