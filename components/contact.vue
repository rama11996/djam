<template lang="pug">
.contact
  .content
    .title  
      h1 Contact
    .summary
      p Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      br
      p Cras erat neque, molestie pharetra urna id, placerat scelerisque urna.  Quisque sed leo felis.
  .contact-form
    form(method="POST" @submit="checkForm()" action="https://formcarry.com/s/2G5WL90Hjj5")
      .name
        .firstname
          label First Name
          span  *
          input(type="text" name="fname", v-model="fname") 
        .lastname
          label Last name
          span  *
          input(type="text" name="lname" v-model="lname")
      .email
        label E-mail
        span  *
        input(type="email" name="email" v-model="email")
      .number
        label Mobile number
        span  *
        input(type="tel" name="number" v-model="number")
      .textarea 
        label  Your Message      
        textarea 
      button.btn(type="submit") Send Message  
  .image  
    img(src="@/assets/images/contact.png")  
</template>
<script>
export default {
  data () {
    return {
      fname: "",
      lname: "",
      email: "",
      number: ""
    }
  },
  methods: {
    checkForm() {
      if(this.fname == "") {
        alert("First Name required")
      }
      if(this.lname == "") {
        alert("Last Name required")
      }
      if(this.email == "") {
        alert("Email required")
      }
      if(this.number == "") {
        alert("Number required")
      }
      else {
        console.log(this.fname)
        console.log(this.lname)
        console.log(this.email)
        console.log(this.number)
      } 
    }
  }
}
</script>
<style lang="sass" scoped>
@import 'assets/styles/includes'
.contact
  position: relative
  @media (min-width: 900px)
    display: flex
  @media (max-width: 900px)
    padding-bottom: 300px
  background-color: #f9f7f3
  .content, .contact-form
    margin: 3rem
  .image
      width: 300px
      height: 300px
      @media (max-width: 900px)
        @include absolute-sw
      @media (min-width: 900px)
        @include absolute-sw  
      

  .content
    .summary
      font-size: 1.7rem
      line-height: 30px
      font-weight: 200 
  .contact-form 
    margin-right: 4rem
    padding: 1rem
    @media (min-width: 900px)
      width: 70%
      @include slideInRight
    input, label
      width: 100%
    .textarea
      textarea
        vertical-align: top  
    .name
      .firstname, .lastname
        padding: 0.5rem
      display: flex
      > div
        flex: 1
      @media (max-width: 1200px)
        display: block  
      
    input, textarea
      margin-right: 1rem
      box-sizing: border-box
     
    button
      @include theme(white, #474F62)
      border: 1px solid transparent
      margin-top: 1rem
      text-align: center
      width: 100%
      &:hover
        background: rgba(#474F62, 0.8) 
    .email, .number, .textarea
      padding: 0.5rem
    span
      color: red  

</style>