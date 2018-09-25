<template lang="pug">
.container
  navigation
  process
  textcarrosel
  imagecarrosel
  pricing
  contact
  footernav
</template>

<script>
import pricing from '../components/pricing'
import contact from '../components/contact'
import process from '../components/process'
import footernav from '../components/footernav'
import textcarrosel from '../components/textcarrosel'
import imagecarrosel from '../components/imagecarrosel'
import navigation from '../components/navigation'

export default {
  components: {
    pricing,
    contact,
    process,
    footernav,
    textcarrosel,
    imagecarrosel,
    footernav,
    navigation
  }
}
</script>

<style lang="sass">

</style>

