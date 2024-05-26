<template>
  <q-layout view="hHh lpR fFf">
    <q-drawer v-model="drawer" side="left" overlay>
      <!-- Isi dari drawer Anda -->
      <q-list>
        <q-item clickable v-ripple>
          <q-item-section>
            Home
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section>
            About
          </q-item-section>
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section>
            Contact
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <div class="q-pa-md">
        <!-- Konten utama Anda di sini -->
        <Carousel />
      </div>
    </q-page-container>

    <Navbar @toggle-drawer="drawer = !drawer" />
    <Footer />
  </q-layout>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Carousel from './components/Corousel.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Footer
  },
  data() {
    return {
      drawer: false
    }
  }
}
</script>

<style>
/* Tambahkan gaya khusus Anda di sini */
</style>
