<template>
  <div id="app">
    <v-app>
      <Navbar/>
      <router-view/>
      <Footer/>
    </v-app>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Footer from '@/components/Footer'
export default {
  components:{
    Navbar,
    Footer
  }
}
</script>
