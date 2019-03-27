<template>
  <div class="container-scroller">
    <NavBar />
    <div class="container-fluid page-body-wrapper">
      <SideNav />
      <div class="main-panel">
        <nuxt />
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from '@/components/Navigation/NavBar'
import SideNav from '@/components/Navigation/SideNav'
import Footer from '@/components/Navigation/Footer'

export default {
  components: {
    NavBar,
    SideNav,
    Footer
  }
}
</script>
