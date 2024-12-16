<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Map from './components/Map.vue'
import City from './components/City.vue'
import Technology from './components/Technology.vue'
import Presentation from './components/Presentation.vue'

</script>

<template>

<Header></Header>
<Main></Main>
<Map></Map>
<City></City>
<Technology></Technology>
<Presentation></Presentation>

</template>

<style>
@font-face {
    font-family: 'MabryPro';
    src: url('./fonts/MabryPro-Bold.ttf') format('truetype'); 
    font-style: normal;
}

@font-face {
    font-family: 'MabryPro';
    src: url('./fonts/MabryPro-Regular.ttf') format('truetype'); 
    font-weight: normal; 
    font-style: normal; 
}

* {
  margin: 0;
  padding: 0;
  
 
}

body, button, select, a {
    font-family: 'MabryPro', sans-serif;
    font-size: 16px;
}

html {
    overflow-x: hidden;
}

</style>
