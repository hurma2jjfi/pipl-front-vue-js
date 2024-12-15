<template>
<div id="icon__present">
<div id="title"><img src="./icons/title.png" alt=""></div>
</div>
<div class="roditel__grid">
    <div class="grid__inner">
        <div id="listbox__label">Дом</div>
        <button id="btn"></button>
        <p id="listbox__title">Любой</p>
    </div>
    <div class="grid__inner">
        <div id="listbox__label">Комнатность</div>
        <button id="btn"></button>
        <p id="listbox__title">Любая</p>
    </div>
    <div class="grid__inner">
        <div id="listbox__label">Площадь</div>
        <button id="btn"></button>
        <p id="listbox__title">Любая</p>
    </div>
    <span><div class="grid__inner">
        <div class="flex__count">
        <a id="count__kvar" href="#">227 квартир</a></div>
        <div class="flex__svg">
        <span class="tailwind-svg-icon text-black text-[22px]"><svg width="22" height="23" viewBox="0 0 22 23" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect y="0.375" width="22" height="22" rx="4" fill="#FDC300"></rect>
<path d="M12.5332 10.2251L16.0337 13.6751L12.5332 17.1251" stroke="currentColor"></path>
<path d="M15.9325 13.675H8.96582C7.30897 13.675 5.96582 12.3319 5.96582 10.675V5.625" stroke="currentColor"></path>
</svg>
</span></div>
    </div></span>
</div>
<div class="grid__lines">
<div class="pointed-heading">
обо мне
</div>
<p class="deviz">Я – жилой квартал ПИПЛ.<br> Нахожусь в одной из лучших<br>  локаций города – у<br> Комсомольской набережной</p>
</div>
<div class="flex__slogan">
<p class="slogan">Каждый день я наслаждаюсь<br> чудесными закатами над<br> величественной Волгой. Давай<br> вместе?</p></div>
<div class="grid__two">
<p class="five__house">5 ДОМОВ</p>
<p class="title__house">5 многоквартирных домов<br> комфорт-класса, где все от<br> людей для людей.
     Я знаю, как<br> современному человеку важно<br> жить в уютном, безопасном,<br> продуманном пространстве</p></div>
<img id="present__second" src="./icons/background.png" alt="">
<section class="section__black__first">
    <div class="grid__container">
    <div class="grid__child child-1">
        <div class="content">
            <h3 class="title">25 тематических<br> зон</h3>
            <p class="description">Открытый кинотеатр и зоны воркаута,<br> детские и спортплощадки, 
                контактный<br> фонтан и амфитеатр – со мной не<br> соскучишься! Питомцы же смогут<br> резвиться в отдельной зоне для<br> выгула</p>
        </div>
    </div>
    <div class="grid__child child-2">
        <div class="content">
            <h3 class="title">Нет преград</h3>
            <p class="description">Открытый кинотеатр и зоны воркаута,<br> детские и спортплощадки, 
                контактный<br> фонтан и амфитеатр – со мной не<br> соскучишься! Питомцы же смогут<br> резвиться в отдельной зоне для<br> выгула</p>
        </div>
    </div>
    <div class="grid__child child-3">
        <div class="content">
            <h3 class="title">Двор без машин</h3>
            <p class="description">Открытый кинотеатр и зоны воркаута,<br> детские и спортплощадки, 
                контактный<br> фонтан и амфитеатр – со мной не<br> соскучишься! Питомцы же смогут<br> резвиться в отдельной зоне для<br> выгула</p>
        </div>
    </div>
    <div class="grid__child child-4">
        <div class="content">
            <h3 class="title">Первый этаж мечты<br></h3>
            <p class="description">Открытый кинотеатр и зоны воркаута,<br> детские и спортплощадки, 
                контактный<br> фонтан и амфитеатр – со мной не<br> соскучишься! Питомцы же смогут<br> резвиться в отдельной зоне для<br> выгула</p>
        </div>
    </div>
</div>
<div class="cnt">
<div class="center__contain">
<div class="pointed-heading-two">
особенности
</div>
<h1 id="want__live">ЗДЕСЬ ХОЧЕТСЯ<br><span class="text__yellow">ЖИТЬ</span></h1></div></div>
<div class="line__yellow__ptrn"><img class="w-ful" src="./icons/yellow-horizontal-line.svg" alt=""></div>
</section>
</template>

<style>

.w-ful {
    width: 100%;
}

.line__yellow__ptrn {
    display: flex;
    justify-content: center;
    margin-top: -270px;
}

.cnt {
    display: flex;
    justify-content: center;
    position: relative;
    top: -160px;
    z-index: 1;
    
}



#want__live {
    font-size: 118px;
    color: #fff;
    font-weight: bolder;
    margin-top: 32px;
    text-align: center; /* Центрируем текст по горизонтали */
    margin: 0; /* Убираем отступы по умолчанию */
}

.text__yellow {
    color: #fdc300;
}

.pointed-heading-two {
    font-size: 14px;
    text-transform: uppercase;
    color: #fff;
    padding-left: 450px;
}

.pointed-heading-two:before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #fff;
}


.grid__container {
    display: flex;
    justify-content: center;
    padding-top: 100px;
    flex-direction: row;
    gap: 20px;
}

.grid__child {
    background: #4a4849; /* Цвет фона по умолчанию */
    width: 307px;
    height: 389px;
    padding: 20px;
    position: relative; /* Для позиционирования текста */
    overflow: hidden; /* Скрываем текст за пределами блока */
    transition: background-color 0.3s ease; /* Плавный переход цвета фона */
}

.grid__child::before {
    content: "";
    background-image: url(./icons/medium_2_kopiya_65e7ac2a59.webp);
    background-position: center;
    background-size: cover; /* Чтобы изображение занимало весь блок */
    position: absolute; /* Абсолютное позиционирование для изображения */
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 1; /* Устанавливаем уровень наложения ниже текста */
    transition: opacity 0.3s ease; /* Плавный переход для прозрачности изображения */
}

.grid__child:hover::before {
    opacity: 0; /* Скрываем изображение при наведении */
}

.content {
    position: relative; /* Относительное позиционирование для текста */
    color: white; /* Цвет текста */
    opacity: 0; /* Скрываем текст по умолчанию */
    transition: opacity 0.3s ease; /* Плавный переход для видимости текста */
}

.grid__child:hover .content {
    opacity: 1; /* Показываем текст при наведении */
}

.grid__child:hover {
    background-color: rgba(99, 95, 95, 0.8); /* Цвет фона при наведении */
}

.title {
    font-size: 32px;
    
}

.description {
    font-size: 14px;
    padding-top: 160px;
    letter-spacing: -.02em;
    line-height: 120%;
    opacity: .7;
}

.grid__child.child-1::before {
    background-image: url(./icons/medium_1_kopiya_ce3b3fac1a.webp); 
}

.grid__child.child-2::before {
    background-image: url(./icons/medium_2_kopiya_65e7ac2a59.webp); 
}

.grid__child.child-3::before {
    background-image: url(./icons/medium_3_c3816cdbb1.webp); 
}

.grid__child.child-4::before {
    background-image: url(./icons/medium_4_a56e308c30.webp); 
}




#present__second {
    position: relative;
    top: 5px;
}

.grid__two {
    display: grid;
    justify-content: center;
    margin-right: -1176px;
    margin-top: 148px;
}

.five__house {
    font-size: 118px;
    letter-spacing: -.05em;
    line-height: 90%;
    color: #282525;
    font-weight: bolder;
    overflow-y: hidden;
}

.title__house {
    font-size: 24px;
    margin-top: 40px;
    /* letter-spacing: -.04em;
    line-height: 90% */
}

#icon__present {
  width: 100%;
  height: 780px;
  background-image: url('./icons/main.webp');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  
}




#title {
    display: flex;
    justify-content: center;
}

.grid__inner {
    width: 276px;
    height: 75px;
    background-color: #fff;
    padding: 12px 32px;
   

}


span .grid__inner {
    background-color: #282525;
}

.roditel__grid {
    display: flex;
    justify-content: center;
    flex-direction: row;
    margin-top: -55px;
}

#title {
    position: relative;
    top: 500px;
}

.grid__inner:hover {
border-bottom: 2px solid #282525;
cursor: pointer;

}

span .grid__inner:hover {
border-bottom: 2px solid #ffffff;
cursor: pointer;

}

#listbox__label {
    font-size: 14px;
    color: rgba(0, 0, 0, .4);
}

#listbox__title {
    font-size: 24px;
}

#count__kvar {
    font-size: 20px;
    text-decoration: underline;
    text-underline-offset: 8px;
    color: #fff;
}

.flex__count {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 20px;
}

.pointed-heading {
    font-size: 14px;
    text-transform: uppercase;
    display: flex; /* Используем flex для выравнивания */
    align-items: center; /* Центрируем элементы по вертикали */
}

.pointed-heading:before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #282525; 
}

.deviz {
    font-size: 62px;
    margin-top: 32px;
    /* letter-spacing: -.04em;
    line-height: 90% */
}

.slogan {
    font-size: 24px;
    /* letter-spacing: -.04em;
    line-height: 90% */
}

.grid__lines {
    display: grid;
    justify-content: center;
    margin-left: -540px;
    padding-top: 180px;
}

.flex__slogan {
    display: grid;
    justify-content: center;
    margin-right: -1009px;
    margin-top: -147px;
}

.section__black__first {
    background-color: #282525;
    width: 100%;
    height: 1000px;
    margin: 0;
    padding: 0;
}
</style>

<script>

// document.addEventListener('DOMContentLoaded', () => {
//     gsap.to('.parallax-strip', {
//     xPercent: 700,
//     duration: 5, // Длительность анимации (секунды)
//     ease: 'none', // Линейное движение
//     repeat: 0, // Бесконечное повторение
//     stagger: 0.5, // Задержка между полосами
//     yoyo: false, // Не возвращать полосы в исходное положение
//   });

//   // Для плавного исчезания на правом краю (опционально):
//   gsap.to('.parallax-strip', {
//     scrollTrigger: {
//       trigger: '#icon__present',
//       start: 'top top',
//       end: '+=780', // Точка окончания триггера с учетом высоты контейнера
//       scrub: 1,
//     },
 
//   })
// });



</script>