<template>
    <section class="presentation__wrapper">
      <h2 class="presentation__title__big">первый этаж</h2>
      <div class="container__top">
        <div class="grid__first__part">
          <div class="cnt__from__blocks">
            <div class="title__big__present">
              <div class="slide-counter">0{{ currentIndex + 1 }}<span>/0{{ slides.length }}</span></div>
              <h4 class="bicycle">{{ slides[currentIndex].title }}</h4>
            </div>
            <div class="desc__big__present fade-in">{{ slides[currentIndex].description }}</div>
          </div>
        </div>
        <!-- Swiper для большого изображения -->
        <swiper
          ref="mySwiper"
          class="mySwiper"
          :pagination="{ clickable: false }"
          :loop="false"
          :effect="'slide'"  
          :speed="900"       
          @swiper="onSwiperInit"
          @slideChange="onSlideChange"
        >
          <swiper-slide v-for="(slide, index) in slides" :key="index">
            <img :src="slide.large" alt="Large Image" class="large-image" />
          </swiper-slide>
        </swiper>
  
        <!-- Карусель для маленьких изображений -->
        <div class="small-images">
          <div v-for="(slide, index) in slides" :key="index" @click="changeSlide(index)">
            <img 
              :src="slide.small" 
              alt="Small Image" 
              :class="{ active: index === currentIndex }" 
            />
          </div>
        </div>
  
        <div class="flex__gap">
          <button class="nav__line" @click="prevSlide" :disabled="currentIndex === 0"><svg width="19" height="19" viewBox="0 0 16 10" fill="currentColor" xmlns="http://www.w3.org/2000/svg" style="transform: rotate(180deg);">
  <path fill-rule="evenodd" clip-rule="evenodd" d="M13.7986 4.49963L10.0966 0.851001L10.8088 0.149048L15.7307 5.00002L10.8088 9.851L10.0966 9.14905L13.7994 5.49963L0.895142 5.49964V4.49964L13.7986 4.49963Z" fill="currentColor"></path>
</svg></button>
          <button class="nav__line" @click="nextSlide" :disabled="currentIndex === slides.length - 1"><svg width="19" height="19" viewBox="0 0 16 10" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M13.7986 4.49963L10.0966 0.851001L10.8088 0.149048L15.7307 5.00002L10.8088 9.851L10.0966 9.14905L13.7994 5.49963L0.895142 5.49964V4.49964L13.7986 4.49963Z" fill="currentColor"></path>
</svg></button>
        </div>
      </div>
      <div class="paddinh"></div>
    </section>
  </template>
  
  
  <script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';
import largeImage1 from '@/components/icons/1_f0bd9a721e.webp';
import smallImage1 from '@/components/icons/2_0fd548ddcd.webp';
import largeImage2 from '@/components/icons/2_0fd548ddcd.webp';
import smallImage2 from '@/components/icons/1_f0bd9a721e.webp';
import largeImage3 from '@/components/icons/2_0fd548ddcd.webp';
import smallImage3 from '@/components/icons/1_f0bd9a721e.webp';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      currentIndex: 0,
      swiperInstance: null,
      slides: [
        { large: largeImage1, small: smallImage1, title: 'Первый слайд', description: 'Описание первого слайда.' },
        { large: largeImage2, small: smallImage2, title: 'Второй слайд', description: 'Описание второго слайда.' },
        { large: largeImage3, small: smallImage3, title: 'Третий слайд', description: 'Описание третьего слайда.' },
      ],
    };
  },
  methods: {
    onSwiperInit(swiper) {
      this.swiperInstance = swiper;
    },
    changeSlide(index) {
      this.currentIndex = index;
      if (this.swiperInstance) {
        this.swiperInstance.slideTo(index);
      }
    },
    prevSlide() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
        if (this.swiperInstance) {
          this.swiperInstance.slideTo(this.currentIndex);
        }
      }
    },
    nextSlide() {
      if (this.currentIndex < this.slides.length - 1) {
        this.currentIndex++;
        if (this.swiperInstance) {
          this.swiperInstance.slideTo(this.currentIndex);
        }
      }
    },
  },
};
</script>

  
  <style scoped>
.slide-counter span {
    color: #282525B3;
}

  .nav__line {
cursor: pointer;

  }
  .nav__line {
    position: relative; /* Для правильного позиционирования псевдоэлемента */
    overflow: hidden; /* Скрываем переполнение */
    border: 1px solid transparent; /* Начальный бордер прозрачный */
    transition: border-color 0.3s ease; /* Плавная анимация изменения цвета бордера */
    border-radius: 5px;
}

.nav__line:hover {
    border-color: black; /* Цвет бордера при наведении */
}

  .container__top {
    position: relative;
    top: -170px;
  }

.cnt__from__blocks {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    position: absolute;
    padding-top: 643px;
    padding-left: 90px;
}

.small-images {
margin-left: 1380px;
margin-top: -100px;
z-index: 1;
}

.flex__gap {
    display: flex;
    justify-content: end;
    position: relative;
    margin-top: -200px;
    margin-right: 100px;
    z-index: 1;
    gap: 15px;
}

.grid__first__part {
    display: grid;
    justify-content: start;
}
  .bicycle {
font-size: 32px;
letter-spacing: -1.28px;
margin: 0px 0px 64px;
  }

  .slide-counter {
    margin: 0px 0px 64px;
  }

  .desc__big__present {
    font-size: 16px;
    color: #282525B3;
    
  }

.presentation__title__big {
font-size: 200px;
color: #E6E5E2;
text-transform: uppercase;
white-space: nowrap;
margin: 0px 0px -40px;
letter-spacing: -10.72px;
padding: 128px 40px;
}

  .presentation__wrapper {
    text-align: center;
  }
  
  .large-image {
    width: 50%; /* Установите желаемую ширину для большого изображения */
    height: auto;
  }
  
  .small-images {
    display: flex;
    justify-content: center;
  }
  
  .small-images img {
    width: 100px; /* Установите желаемую ширину для маленьких изображений */
    height: auto;
    margin: 0 5px; /* Отступы между маленькими изображениями */
  }
  
  .small-images img {
    transition: border-left 0.3s ease, transform 0.3s ease; /* Плавный переход для рамки и трансформации */
}

.small-images img.active {
    border-left: 3px solid #000000; /* Рамка для активного миниатюры */
    transform: scale(1.1); /* Увеличение размера активного миниатюры */
}
  
  .slide-counter {
    margin-top: 10px;
  }
  
  button {
    margin-top: 10px;
  }

  .nav__line {
    width: 40px;
    height: 40px;
    padding: 10px;
  }

  .paddinh {
    padding: 128px 40px;
  }
 
  </style>
  