<template>
<div class="title__blag">Благоустройство</div>
<div class="bolder__text"><h1>Город эмоций</h1></div>
<div class="medium__center">
<span class="medium__desc">Мой двор – Город эмоций. Каждый метр<br> продуманного пространства и элемент окружения<br>
     – это портал в мир безграничного воображения!</span></div>
<div class="image__preview">
    <img src="./icons/bg.webp" alt="">
</div>
<div class="obertka__btnsvg">
<button
    class="btn"
    @mouseover="hover = true"
    @mouseleave="hover = false"
    :class="{ 'hover': hover }"
  >
    <slot>Посмотреть все площадки</slot>
  </button>
  <div class="icon__slot"><svg width="22" height="23" viewBox="0 0 22 23" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect y="0.375" width="22" height="22" rx="4" fill="#FDC300"></rect>
<path d="M12.5332 10.2251L16.0337 13.6751L12.5332 17.1251" stroke="currentColor"></path>
<path d="M15.9325 13.675H8.96582C7.30897 13.675 5.96582 12.3319 5.96582 10.675V5.625" stroke="currentColor"></path>
</svg></div></div>
</template>

<style>
.obertka__btnsvg {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0px 0px 170px;
}

.icon__slot {
    margin: 35px 10px 26px;
}

.image__preview {
    display: flex;
    justify-content: center;
}

.bolder__text {
    display: flex;
    justify-content: center;
    color: #282525;
    font-size: 36px;
    margin: 0px 0px 32px;
    text-transform: uppercase;
    letter-spacing: -.02em;
    font-weight: bold;

}

.medium__desc {
    font-size: 16px;
    letter-spacing: -.02em;
    line-height: 120%;
    opacity: .7;
    margin: 0px 0px 32px;
}

.medium__center {
    display: flex;
    justify-content: center;
}
.title__blag {
    text-transform: uppercase;
    font-size: 16px;
    margin: 0px 0px 32px;
}

.title__blag::before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #282525;
}

.title__blag {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 170px;
}


</style>

<script>
export default {
  data() {
    return {
      hover: false,
    
    };
  },
};
</script>