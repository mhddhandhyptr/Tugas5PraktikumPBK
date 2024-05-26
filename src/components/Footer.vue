<template>
    <q-footer class="custom-footer">
      <q-toolbar>
        <q-toolbar-title class="footer-title">
          @Muhammad Dhandhy Putera Irvantie <br>
          ig : sneakyboyy.motor
        </q-toolbar-title>
        <q-btn
          icon="fab fa-instagram"
          color="white"
          size="md"
          @click="redirectToInstagram"
          class="instagram-btn"
        />
      </q-toolbar>
    </q-footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    methods: {
      redirectToInstagram() {
        window.open('https://www.instagram.com/mhddhandhyptr/', '_blank');
      }
    }
  }
  </script>
  
  <style scoped>
  .custom-footer {
    background-color: #1976D2; /* Warna latar belakang footer */
    color: white; /* Warna teks footer */
  }
  
  .footer-title {
    font-size: 18px; /* Ukuran teks judul */
  }
  
  .instagram-btn {
    margin-left: 10px; /* Spasi antara ikon Instagram dan teks judul */
  }
  </style>
  