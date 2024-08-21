<template>
  <Header />
  <Body />
  <Footer />
</template>

<script>
import MainHeader from './MainHeader.vue'
import MainContainer from './MainContainer.vue'
import Footer from './Footer.vue'
export default {
  name: 'HomePage',
  components: {
    Header: MainHeader,
    Body: MainContainer,
    Footer
  }
}
</script>

<style></style>
