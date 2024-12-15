<template>
<section id="map">
<div class="map__end">
<div id="map__background"><div class="flex__point">
    <p class="pointed__one">ИНФРАСТРУКТУРА</p>
    <p class="title__point">Полезное<br> рядом</p>
    <span class="description__poi">А сейчас загадай всё, что тебе нужно для<br> комфортной жизни… Вуаля! 
        Теперь это всё<br> находится буквально через дорогу от тебя!</span>
        <div class="btn__star">
        <button
    class="btn"
    @mouseover="hover = true"
    @mouseleave="hover = false"
    :class="{ 'hover': hover }"
  >
    <slot>Посмотреть все на карте</slot>
  </button></div>
</div><div class="map__end__flex">
    

    <div class="circle__wrapper" @mouseenter="showInfo = true" @mouseleave="showInfo = false">
    <span class="ellipse__yellow">
      <span class="ellipse__black"></span>
    </span>
    <div class="name__architecture">Центральный стадион</div>
    <transition name="fade">
      <div v-if="showInfo" class="info-box">
        <h3 class="info-title">Центральный<br> стадион</h3>
        <p class="info-description">10 минут пешком</p>
        <img width="250px" height="150px" src="./icons/0.webp" alt="Map Image" class="info-image" />
      </div>
    </transition>
  </div>

  

    <img id="map__img" src="./icons/mapbackground.png" alt="">
</div></div></div>

</section>
</template>

<style>

.info-description {
    padding: 20px 0px 40px;
    font-size: 14px;
    text-transform: lowercase;
}

.info-box {
  position: absolute; /* Positioning it absolutely within the wrapper */
  top: -10px; /* Adjust as necessary to position it above or below the circle */
  left: calc(100% + 10px); /* Position it to the right of the circle */
  background-color: white; /* Background color for info box */
  padding: 10px; /* Padding inside the box */
  box-shadow: 0px 2px 5px rgba(0,0,0,0.2); /* Shadow for depth */
}

/* Transition Effects */
.fade-enter-active, .fade-leave-active {
    transition: opacity .3s ease;
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
    opacity: 0;
}

.name__architecture {
    margin: 0px 0px 0px 4px;
    padding: 4px;
    background: #F1F1ED;
    border-radius: 5px;
}

.circle__wrapper {
    display: flex;
    align-items: center;
    position: absolute;
    margin-top: 100px;
    margin-left: 299px;
}

.ellipse__yellow {
    width: 22px;
    height: 22px;
    background: #FDC300;
    border-radius: 50%;
    display: inline-block;
    position: relative;
    cursor: pointer; 
}

.ellipse__black {
    width: 10px;
    height: 10px;
    background: #282525;
    border-radius: 50%;
    display: inline-block;
    position: absolute; 
    top: 50%; 
    left: 50%; 
    transform: translate(-50%, -50%); 
}

.name__architecture {
    text-transform: uppercase;
    font-size: 12px;
}



#map__background {
    width: 100%;
    height: 834px;
    background-color: #F1F1ED; 
}

.map__end {
    display: flex;
    justify-content: end;
}

.map__end__flex {
    position: relative;
    margin-left: 850px;
    margin-top: -554px;
}

.btn {
  position: relative;
  background-color: transparent;
  border: none;
  color: currentColor;
  text-decoration: none;
  font-size: 16px; 
  cursor: pointer;
  transition: color .3s;
}

.btn::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -2px; /* Adjust this value to position closer to text */
  left: 0px;
  width: 100%;
  height: 1px;
  background-color: currentColor;
  transform: scaleX(1); /* Start fully visible */
  transition: transform .3s ease; /* Transition for smooth effect */
}

.btn.hover::after {
  transform: scaleX(0); /* Scale down to disappear on hover */
}

.flex__point {
    display: grid;
    padding: 140px 40px;
}

.pointed__one {
    font-size: 14px;
    margin: 0px 0px 24px;
}

.pointed__one:before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #282525;
}

.title__point {
    font-size: 62px;
    margin: 0px 0px 56px;
    letter-spacing: -.04em;
    line-height: 90%;
}

.description__poi {
    font-size: 16px;
    letter-spacing: -.02em;
    line-height: 120%;
    opacity: .7;
    margin: 0px 0px 32px;
}

.btn {
    font-size: 16px;

}

.btn__star {
    display: flex;
    justify-content: start;
}

</style>

<script>
export default {
  data() {
    return {
      hover: false,
      showInfo: false,
    };
  },
};
</script>