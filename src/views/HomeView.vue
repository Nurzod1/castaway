<template>
  <div class="home">
    <Navbar v-model="isSidebarOpen"/>
    <Sidebar :active="isSidebarOpen"/>
    <Header />
    <Episodes />
    <Subscribe />
    <Subtitle />
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Sidebar from '@/components/Sidebar.vue'
import Header from '@/components/Header.vue'
import Episodes from '@/components/Episodes.vue'
import Subscribe from '@/components/Subscribe.vue'
import Subtitle from '@/components/Subtitle.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: { Navbar, Sidebar, Header, Episodes, Subscribe, Subtitle, Footer },
  name: 'HomeView',
  data() {
    return {
      isSidebarOpen: false,
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
