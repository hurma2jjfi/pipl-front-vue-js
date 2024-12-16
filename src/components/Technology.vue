<template>
<section class="technology__wrapper">
    <div class="container__center">
    <div class="container__double">
<div class="wr__tit">
    <p>архитектурная концепция</p>
</div>
<div class="wr__zag">
    <h1>
      {{ displayedText }}<span v-if="isCursorVisible" class="cursor">|</span>
    </h1>
  </div></div>
<div class="wr__desc">
    Суть моей архитектурной идеи –<br> естественность и долговечность, классика и <br>современность. 
    Это лаконичные формы,<br> минималистичные фасады без лишнего<br> визуального шума, тщательный подбор<br> кирпича для отделки фасадов, оттенков и <br>прочности.
     Я о тебе позаботился – <br> повышенная теплоизоляция за счет<br> керамического термоблока и улучшенная<br> звукоизоляция стен
</div>
<div class="wr__image">
    <img
        width="900px"
        height="1022px"
        src="./icons/1_5f17e14589.webp"
        alt=""
        @mouseover="zoomIn"
        @mouseleave="zoomOut"
        :class="{ 'zoom-in': isZoomed }"
      />
</div>
</div>
<div class="line__yel"><img src="./icons/yellow-horizontal-line.svg" alt=""></div>

<div class="li__center">
<ul class="ul">
    <img width="305px" height="305px" src="./icons/vhodnaya_gruppa_jpeg_1_408428fd45.jpg" alt="" id="present__img">
    <li id="li">Экологичные материалы</li>
    <li id="li">Минимализм и эстетика</li>
    <li id="li">Витражное остекление</li>
</ul></div>
</section>
</template>

<style>
.li__center {
display: flex;
justify-content: end;
padding-right: 250px;
margin-top: -672px;
}

#li {
    position: relative; /* Позволяет псевдоэлементу позиционироваться относительно элемента */
    font-size: 24px;
    padding: 12px 0; 
    color: #e0e0dc;
    list-style: none;
}

#li::after {
    content: ""; /* Создает пустой контент для псевдоэлемента */
    display: block; /* Отображает псевдоэлемент как блочный элемент */
    width: 150%; /* Установите желаемую ширину границы (например, 80%) */
    height: 1px; /* Высота границы */
    background-color: #fff; /* Цвет границы */
    margin: 0 auto; /* Центрирует границу по горизонтали */
    position: absolute; /* Позволяет позиционировать границу относительно родителя */
    bottom: 0; /* Устанавливает границу внизу элемента списка */
    left: 0; /* Начало границы от левого края элемента */
}

#li:hover {
    color: #fff;
    cursor: pointer;
}



.line__yel {
display: flex;
justify-content: center;
margin-top: -600px;
}

.line__yel img {
    width: 100%;
}
.container__center {
    padding: 130px 40px;
}

.wr__image {
    display: grid;
    justify-content: center;
    padding-right: 917px;
    margin-top: -215px;

}

.wr__desc {
    display: flex;
    justify-content: center;
    padding-left: 368px;
    padding-top: 80px;
}

.container__double {
    display: flex; /* Создание flex-контейнера */
    justify-content: space-between; /* Выравнивание элементов по основной оси */
    align-items: flex-start; /* Выравнивание элементов по вертикали */
}

.wr__tit {
    width: 50%; /* Задайте ширину для заголовка */
    margin: 15px 0px 54px;
}

.wr__zag {
    width: 49%; /* Задайте ширину для описания */
}

.wr__zag {
    font-size: 32px;
    color: #fff;
}

.technology__wrapper {
    background-color: #282525;
    width: 100%;
    height: 1378px;
    padding: 130px 40px;
}

.wr__desc {
    color: #fff;
    font-size: 16px;
}

.wr__tit {
    color: #fff;
    text-transform: uppercase;
    display: flex;
    align-items: center;
    font-size: 14px;
}

.wr__tit::before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #ffffff;
}

.cursor {
  display: inline-block;
  animation: blink 1s step-end infinite; /* Для плавного мигания курсора */
}

@keyframes blink {
  50% {
    opacity: 0; /* Курсор исчезает на половину времени */
  }
}
.wr__image {
  width: 900px; /* Ширина блока изображения */
  height: 1022px; /* Высота блока изображения */
  overflow: hidden; /* Скрыть часть изображения, выходящую за пределы блока */
  position: relative; /* Относительное позиционирование для правильного отображения */
}

.wr__image img {
  width: 100%; /* Ширина изображения на 100% от блока */
  height: auto; /* Автоматическая высота для сохранения пропорций */
  transition: transform 0.5s ease; /* Плавный переход для эффекта увеличения */
}

.zoom-in {
  transform: scale(1.1); /* Увеличение изображения на 10% */
}

.wr__zag h1 {
  color: white; /* Настройте цвет текста по вашему желанию */
}

.cursor {
  display: inline-block;
  animation: blink 1s step-end infinite; /* Для плавного мигания курсора */
}

@keyframes blink {
  50% {
    opacity: 0; /* Курсор исчезает на половину времени */
  }
}

#present__img {
margin-bottom: 30px;

}

</style>

<script>
import gsap from 'gsap';
gsap.registerPlugin(ScrollTrigger);

export default {
  data() {
    return {
      fullText: 'Высокие технологии строительства и продуманный внешний вид',
      displayedText: '',
      currentIndex: 0,
      typingSpeed: 100, // скорость печатания в миллисекундах
      isCursorVisible: true, // состояние видимости курсора
      isZoomed: false, // состояние увеличения изображения
    };
  },
  mounted() {
    this.typeText();
    this.blinkCursor();
  },
  methods: {
    typeText() {
      if (this.currentIndex < this.fullText.length) {
        this.displayedText += this.fullText.charAt(this.currentIndex);
        this.currentIndex++;
        setTimeout(this.typeText, this.typingSpeed);
      }
    },
    blinkCursor() {
      setInterval(() => {
        this.isCursorVisible = !this.isCursorVisible;
      }, 500); // мигание курсора каждые 500 мс
    },
    zoomIn() {
      this.isZoomed = true; // Увеличиваем изображение при наведении
    },
    zoomOut() {
      this.isZoomed = false; // Возвращаем в исходное состояние при уходе курсора
    },
  },
};


function animateText() {
    const textElement = document.querySelector('.wr__desc'); 
    const imageElement = document.querySelector('.wr__image'); 
    const listElement = document.querySelector('ul'); 

    
    gsap.from(textElement, {
        duration: 2,      
        y: 50,            
        opacity: 0,       
        ease: "power2.out", 
        scrollTrigger: {
            trigger: textElement, 
            start: "top 80%",     
            toggleActions: "play none none reverse" 
        }
    });

   
    gsap.from(imageElement, {
        duration: 2,      
        y: 50,            
        opacity: 0,       
        ease: "power2.out", 
        scrollTrigger: {
            trigger: imageElement, 
            start: "top 80%",      
            toggleActions: "play none none reverse"
        }
    });

 
    gsap.from(listElement, {
        duration: 2,      
        y: 50,            
        opacity: 0,       
        ease: "power2.out", 
        scrollTrigger: {
            trigger: listElement, 
            start: "top 80%",      
            toggleActions: "play none none reverse" 
        }
    });
}



window.onload = () => {
    animateText();
};

</script>