<template>
  <div class="carousel-container">
    <q-carousel
      v-model="slide"
      swipeable
      animated
      infinite
      :height="'100vh'"
      :autoplay="3000"
    >
      <q-carousel-slide
        v-for="(img, index) in images"
        :key="index"
        :name="index"
        :img-src="img.src"
        contain
      />
    </q-carousel>
    <div class="caption-container">
      <div class="caption-text">{{ images[slide].caption }}</div>
    </div>
    <div class="absolute-bottom">
      <q-btn round color="primary" class="nav-button" @click="prevSlide">
        <q-icon name="chevron_left" />
      </q-btn>
      <q-btn round color="primary" class="nav-button" @click="nextSlide">
        <q-icon name="chevron_right" />
      </q-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      images: [
        {
          src: 'https://imgcdn.oto.com/large/gallery/color/73/2569/honda-vario-160-color-484282.jpg',
          caption: 'Honda Vario 160 '
        },
        {
          src: 'https://imgcdn.oto.com/large/gallery/color/84/2260/yamaha-nmax-155-color-418900.jpg',
          caption: 'Yamaha N-Max 155 '
        },
        {
          src: 'https://ic1.maxabout.us/news/2023/01/2022122614444694822Q97419.png',
          caption: 'Yamaha XSR 155 '
        },
        {
          src: 'https://images.hindustantimes.com/auto/img/2023/09/26/600x338/2024_Yamaha_R15_V4_Japan_1695745529444_1695745534261.jpg',
          caption: 'Yamaha R15 155 '
        },
        {
          src: 'https://imgcdn.zigwheels.ph/large/gallery/color/86/1832/yamaha-mio-aerox-color-946812.jpg',
          caption: 'Yamaha Aerox 155 '
        },
        {
          src: 'https://hondausareview.com/wp-content/uploads/2023/01/Screenshot_4-780x470.png',
          caption: 'Honda Scoopy 110 '
        }
      ]
    }
  },
  methods: {
    prevSlide() {
      this.slide = (this.slide - 1 + this.images.length) % this.images.length
    },
    nextSlide() {
      this.slide = (this.slide + 1) % this.images.length
    }
  }
}
</script>

<style scoped>
.carousel-container {
  position: relative;
  width: 100%;
  overflow: hidden; /* Mengatasi overflow dari carousel */
}

.caption-container {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.7); /* Meningkatkan opacity untuk sedikit transparan */
  color: white;
  padding: 10px;
  text-align: center;
}

.caption-text {
  font-size: 20px; /* Meningkatkan ukuran teks */
}

.absolute-bottom {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
}

.nav-button {
  margin: 0 10px; /* Menambahkan sedikit ruang di antara tombol navigasi */
}
</style>
