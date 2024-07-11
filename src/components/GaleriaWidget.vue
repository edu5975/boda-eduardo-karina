<template>
  <div class="confirmacion-widget container my-4">
    <h2 class="text-center"><i class="fas fa-heart"></i> Nosotros</h2>
    <Carousel id="gallery" :items-to-show="1" :wrap-around="false" v-model="currentSlide">
      <Slide v-for="(imagen, index) in imagenes" :key="index">
        <div class="carousel__item" >            
            <img class="d-block w-100 galeria-img"  :src="imagen" :alt="'Slide' + index">
        </div>
      </Slide>
    </Carousel>
    <Carousel
      id="thumbnails"
      :items-to-show="7"
      :wrap-around="true"
      v-model="currentSlide"
      ref="carousel"
    >
      <Slide v-for="(imagen, index) in imagenes" :key="index">
        <div class="carousel__item" @click="slideTo(index)">
            <img class="d-block w-100 img-fluid galeria-min-img "  :src="imagen" :alt="'Slide' + index">
        </div>
      </Slide>
    </Carousel>
  </div>
</template>
  
<script>
  import { defineComponent } from 'vue'
  import { Carousel, Slide } from 'vue3-carousel'
  
  import 'vue3-carousel/dist/carousel.css'
  
  export default defineComponent({
    name: 'GalleryWidget',
    components: {
      Carousel,
      Slide,
    },
    data: () => ({
      currentSlide: 0,
      imagenes: [
        require('@/assets/foto1.jpg'), 
        require('@/assets/foto2.jpg'),
        require('@/assets/foto3.jpg'),
        require('@/assets/foto4.jpg'),
        require('@/assets/foto5.jpg'),
        require('@/assets/foto6.jpg'),
        require('@/assets/foto7.jpg'),
        require('@/assets/foto8.jpg'),
        require('@/assets/foto9.jpg'),
        require('@/assets/foto10.jpg'),
        require('@/assets/foto11.jpg'),
      ]
    }),
    methods: {
      slideTo(val) {
        this.currentSlide = val
      },
    },
  })
</script>

<style scoped>

  img {
    border-radius: 5px;
  }

  .galeria-img {
    height: 350px; 
    object-fit: cover;
  }

  .galeria-min-img {
    height: 100px;
    object-fit: cover;
  }
</style>