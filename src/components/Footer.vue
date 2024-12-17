<template>
<footer class="footer">
<div class="center__footer">
<div class="grid__container__fot">
<h5 class="checkpoint__ellipse">поможем сделать правильный выбор</h5>
 <div class="happy__new__year" ref="snowContainer" style="position: relative; overflow: hidden;">
<img class="hover__happy" width="83px" height="53.33px" src="./icons/objects.svg">
  </div>
<h1 class="personal__presentation">Персональная презентация</h1>
<div class="input__row">
<input type="text" name="name" id="name__field" placeholder="Имя">
<input type="text" name= "number" id="number__field"  v-model="phoneNumber"
@input="applyMask" placeholder="Номер телефона*">
<div class="btn__ta">
    <div class="custom-select">
<button id="listbox__btn" @click="toggleDropdown">
<span class="tailw__first">{{ selectedOption }}</span>
<span class="tailw__second"><svg class="back__icon__foot" width="22" height="22" viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg" :class="{ rotate: isOpen }">
<path d="M15.25 9.24219L11.0074 13.4848L6.76472 9.24219" stroke="currentColor"></path>
</svg></span>
</button><div v-if="isOpen" class="dropdown">
      <ul>
        <li v-for="option in options" :key="option" @click="selectOption(option)">
          {{ option }}
        </li>
      </ul>
    </div></div></div></div>
<div class="obertka__foote">
<div class="btn__cont__flex__footer">
<button id="zapis" type="submit">Записаться</button></div>
<div class="copyrighting__fl">
<p class="click">Нажимая на кнопку, вы соглашаетесь с <a id="copyright" href="#">Политикой конфиденциальности</a></p></div></div>



<div class="grid__gap">
<h5 class="checkpoint__ellipse">Офис продаж</h5>
<h5 class="number__reklam">8(8512) 480 480</h5>
<h5 class="city__title__footer">Астрахань, ул. <br>Савушкина, 6к1</h5>
<p class="work">
Пн-Чт: 09:00 – 19:00<br>
Пт: 9:00 – 17:30<br>
Сб: 10:00 – 17:00</p>
<p class="copyright__footer__word">© Киря 2024</p>
<a href="#" class="check__to__map">Посмотреть на карте</a>
<div class="flex__links">
    <div class="link"><a href="#"><svg width="20" height="21" viewBox="0 0 20 21" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M19.8979 15.597C19.8792 15.5453 19.8536 15.4967 19.8217 15.4527C19.2803 14.5458 18.6128 13.7296 17.8414 13.0312L17.8109 13.0152V12.9991H17.7805C17.3387 12.5501 17.0645 12.2454 16.9427 12.1011C16.7407 11.8595 16.6821 11.5201 16.7903 11.2191C17.0554 10.704 17.3721 10.2202 17.7348 9.77583C18.0242 9.39096 18.2375 9.08627 18.405 8.84572C19.6085 7.17795 20.1264 6.10351 19.9741 5.63846L19.9131 5.52621C19.8259 5.43473 19.7143 5.37323 19.5932 5.34981C19.3746 5.28856 19.146 5.27762 18.923 5.31773L15.922 5.33377C15.8511 5.31612 15.7766 5.32172 15.7088 5.34981C15.6624 5.35711 15.6166 5.36783 15.5717 5.38188L15.526 5.39791L15.4803 5.44602C15.4372 5.47456 15.4007 5.51292 15.3736 5.55828C15.3261 5.61417 15.2898 5.67964 15.267 5.75071C14.9578 6.59791 14.586 7.41828 14.155 8.20427C13.896 8.65329 13.6523 9.05419 13.439 9.37492C13.2782 9.63383 13.1 9.88034 12.9059 10.1126C12.7822 10.2501 12.6499 10.3787 12.5098 10.4975C12.4331 10.5664 12.3364 10.606 12.2356 10.6097L12.0528 10.5616C11.9582 10.4966 11.8799 10.4086 11.8243 10.305C11.7615 10.1687 11.7203 10.0224 11.7024 9.87205C11.6872 9.69565 11.672 9.55132 11.672 9.42303V8.90987C11.6872 8.68536 11.6872 8.525 11.6872 8.44481C11.6872 8.1722 11.6872 7.86751 11.7024 7.54678C11.7177 7.22605 11.7177 6.96947 11.7329 6.77704V6.16766C11.733 6.00143 11.7228 5.83537 11.7024 5.67053C11.6739 5.55073 11.6382 5.4329 11.5958 5.31773C11.5458 5.2151 11.4725 5.12699 11.3826 5.06115C11.2737 4.99398 11.1554 4.94527 11.0322 4.91683C10.5671 4.80978 10.0915 4.76133 9.61551 4.7725C8.77995 4.70438 7.93952 4.79123 7.1325 5.02908C6.98083 5.11299 6.84627 5.2274 6.73644 5.36584C6.61457 5.52621 6.59934 5.60639 6.69074 5.62242C7.03113 5.65195 7.34759 5.81852 7.57426 6.08748L7.63519 6.2318C7.69985 6.39105 7.74589 6.55799 7.77229 6.72893C7.83333 6.99175 7.86906 7.26038 7.87892 7.53075C7.90959 7.98453 7.90959 8.44004 7.87892 8.89383C7.83322 9.2787 7.80276 9.56736 7.77229 9.77583C7.75112 9.95311 7.70491 10.1261 7.63519 10.289C7.57426 10.4173 7.52856 10.4975 7.51333 10.5295L7.4524 10.5937C7.36407 10.6252 7.27147 10.6415 7.1782 10.6418C7.04614 10.6295 6.91975 10.5796 6.8126 10.4975C6.65907 10.3661 6.51638 10.2212 6.38607 10.0645C6.19621 9.83631 6.02785 9.58926 5.88338 9.32681C5.70058 9.00609 5.50255 8.62121 5.30452 8.18823L5.13695 7.86751C5.03032 7.65904 4.89322 7.37038 4.71043 6.96947C4.52763 6.56857 4.36006 6.19973 4.22296 5.84693C4.18223 5.70356 4.09625 5.57911 3.97923 5.49413L3.9183 5.46206C3.87056 5.41635 3.81309 5.38335 3.75074 5.36584C3.67663 5.33702 3.60014 5.31554 3.52224 5.3017L0.658404 5.31773C0.440473 5.28753 0.221442 5.36439 0.0643103 5.52621L0.033844 5.59035C0.00461867 5.64367 -0.00614778 5.70601 0.00337768 5.76675C0.0047186 5.86634 0.0254571 5.96459 0.0643103 6.0554C0.475606 7.08173 0.932601 8.07598 1.42006 9.03816C1.90752 10.0003 2.33405 10.754 2.69965 11.3474C3.06524 11.9407 3.43084 12.4699 3.79644 12.9991C4.16203 13.5283 4.421 13.8491 4.54286 13.9934C4.63204 14.1073 4.72876 14.2145 4.83229 14.3141L5.09125 14.5707C5.32204 14.8003 5.56625 15.0146 5.82245 15.2121C6.14234 15.4527 6.50794 15.6932 6.904 15.9338C7.33535 16.1878 7.7962 16.3819 8.27499 16.5111C8.76539 16.6549 9.27463 16.7145 9.78307 16.6875H10.9865C11.1927 16.6887 11.3906 16.602 11.5349 16.4469L11.5806 16.3988C11.6583 16.2406 11.6951 16.0636 11.6872 15.8857C11.6793 15.6054 11.7049 15.3253 11.7634 15.0518C11.7912 14.8494 11.8531 14.6539 11.9462 14.4745C12.0009 14.3565 12.0729 14.2483 12.1594 14.1537C12.2132 14.0919 12.2747 14.0379 12.3422 13.9934C12.3658 13.9785 12.3916 13.9676 12.4184 13.9613C12.6294 13.9123 12.85 13.9718 13.0125 14.1217C13.2511 14.3055 13.4662 14.5212 13.6523 14.7631C13.8503 15.0037 14.0788 15.2923 14.353 15.613C14.5785 15.8634 14.8231 16.0941 15.0842 16.3026L15.2975 16.4309C15.4668 16.5416 15.652 16.6228 15.8459 16.6714C16.0302 16.7457 16.2298 16.7678 16.4247 16.7356L19.0905 16.6875C19.3005 16.697 19.5095 16.653 19.6999 16.5592C19.8211 16.4977 19.9142 16.3881 19.9588 16.2545C19.987 16.1338 19.9922 16.0085 19.9741 15.8857C19.9537 15.7881 19.9283 15.6917 19.8979 15.597Z" fill="currentColor"></path>
</svg></a></div>
    <div class="link"><a href="#"><svg width="20" height="21" viewBox="0 0 20 21" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M15.2389 14.459C15.022 15.073 14.1598 15.5809 13.4722 15.7294C13.0015 15.8294 12.3877 15.9084 10.3195 15.0514C7.9966 14.089 4.771 10.6609 4.771 8.37959C4.771 7.21824 5.4406 5.86592 6.6115 5.86592C7.1749 5.86592 7.2991 5.8769 7.4845 6.32163C7.7014 6.84559 8.2306 8.13651 8.2936 8.26885C8.5537 8.81171 8.02899 9.1295 7.64829 9.60215C7.52679 9.74438 7.3891 9.89822 7.543 10.1629C7.696 10.4222 8.2252 11.2846 9.0028 11.977C10.0072 12.8718 10.8217 13.1575 11.1133 13.2791C11.3302 13.3691 11.5894 13.3481 11.7478 13.1789C11.9485 12.9619 12.1978 12.6019 12.4516 12.2472C12.6307 11.9933 12.8584 11.9616 13.0969 12.0517C13.258 12.1075 15.3055 13.0584 15.3919 13.2105C15.4558 13.3212 15.4558 13.845 15.2389 14.459ZM10.0018 1.75H9.99729C5.03559 1.75 1 5.78682 1 10.75C1 12.718 1.63451 14.5438 2.71361 16.0248L1.5922 19.369L5.05091 18.2638C6.47381 19.2055 8.1721 19.75 10.0018 19.75C14.9635 19.75 19 15.7132 19 10.75C19 5.78682 14.9635 1.75 10.0018 1.75Z" fill="currentColor"></path>
</svg></a></div>
    <div class="link"><a href="#"><svg width="20" height="21" viewBox="0 0 18 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path d="M17.9487 1.82606L15.2323 14.6363C15.0272 15.5403 14.493 15.7653 13.7337 15.3397L9.59453 12.2897L7.5976 14.2107C7.37644 14.4319 7.19192 14.6164 6.76566 14.6164L7.06333 10.4014L14.7341 3.47002C15.0678 3.17298 14.6614 3.00775 14.2159 3.30543L4.73273 9.27692L0.65015 7.99878C-0.23773 7.72168 -0.253803 7.1109 0.835313 6.68464L16.8036 0.53249C17.543 0.255389 18.1898 0.696436 17.9487 1.82606Z" fill="currentColor"></path>
</svg></a></div>
</div>
</div>
<div class="links__last">
<div class="link__politics"><a href="#">Политика конфиденциальности</a></div>
<div class="link__politics"><a href="#">Сделано в России</a></div>
</div>

<div class="links__lev__part">
    <div class="link__f"><a href="#">Квартиры</a></div>
    <div class="link__f"><a href="#">Паркинг</a></div>
    <div class="link__f"><a href="#">Кладовые</a></div>
    <div class="link__f"><a href="#">Коммерция</a></div>
    <div class="link__f"><a href="#">Способы покупки</a></div>
</div>
</div></div>

<div class="button__obertka">
<div class="pulse__ellipse">
<button id="click__me">
<svg width="18" height="18" viewBox="0 0 18 18" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path d="M17.4466 14.1755C17.6569 14.3865 17.8146 14.644 17.9068 14.9273C17.999 15.2106 18.0232 15.5116 17.9775 15.806C17.9318 16.1004 17.8173 16.3798 17.6435 16.6217C17.4696 16.8637 17.2413 17.0613 16.9768 17.1985C15.4658 18.0061 13.7054 18.2125 12.0486 17.7763C7.65125 16.6693 1.33069 10.3487 0.223717 5.95145C-0.212481 4.29463 -0.00608507 2.53415 0.801504 1.02316C0.938748 0.758743 1.13633 0.530368 1.37826 0.356523C1.62018 0.182678 1.89964 0.0682488 2.19402 0.0225019C2.48839 -0.023245 2.78941 0.00097606 3.07268 0.093204C3.35595 0.185432 3.61352 0.343074 3.82454 0.553366L5.701 2.42892C5.9716 2.69681 6.15471 3.04038 6.2262 3.41438C6.29769 3.78839 6.25421 4.17527 6.10149 4.52408C5.93436 4.91542 5.69706 5.2729 5.4013 5.57885C3.25575 7.72441 10.2765 14.7451 12.4211 12.5987C12.7271 12.3019 13.0849 12.0637 13.4768 11.8958C13.8256 11.7428 14.2125 11.6992 14.5866 11.7707C14.9606 11.8422 15.3042 12.0255 15.572 12.2963L17.4466 14.1755Z" fill="currentColor"></path>
</svg></button></div></div>

</footer>
</template>

<style>
.button__obertka {
    position: fixed; /* Use fixed positioning to keep it in view */
    right: 20px; /* Distance from the right edge */
    bottom: 20px; /* Distance from the bottom edge */
    z-index: 1000; /* Ensure it's above other elements */
}

        #click__me {
    background: none;
    border: none;
    cursor: pointer; /* Change cursor to pointer to indicate it's clickable */
}

.pulse__ellipse {
    width: 40px; /* Size of the circle */
    height: 40px; /* Size of the circle */
    background-color: rgb(247, 208, 36); /* Circle color */
    border-radius: 50%; /* Make it circular */
    display: flex;
    justify-content: center; /* Center icon horizontally */
    align-items: center; /* Center icon vertically */
    animation: pulse 1.5s infinite; /* Pulsing animation */
    box-shadow: 0 0 20px rgba(255, 255, 0, 0.5); /* Glow effect */
}

@keyframes pulse {
    0% {
        transform: scale(1);
        opacity: 1;
        background-color: rgb(247, 208, 36); /* Original color */
    }
    50% {
        transform: scale(1.15); /* Slightly grow more */
        opacity: 0.9; /* Slightly fade */
        background-color: rgb(255, 220, 80); /* Lighter color for effect */
    }
    100% {
        transform: scale(1);
        opacity: 1;
        background-color: rgb(247, 208, 36); /* Original color */
    }
}



.links__last {
display: grid;
position: relative;
top: 17px;
}

.link__politics a {
    color: #fff;
    font-size: 14px;
}

.link__f a {
    color: #fff;
    text-decoration: none;
    font-size: 14px;
}

.links__lev__part {
    display: flex;
    flex-direction: row-reverse;
    justify-content: end;
    gap: 30px;
}

.checkpoint__ellipse {
    font-size: 14px;
    font-style: inherit;
}

.grid__gap {
    display: flex;
    flex-direction: row;
    gap: 30px;
    padding-top: 30px;
}

.check__to__map, .number__reklam, .city__title__footer, .work, .copyright__footer__word {
    color: #fff;
}

.link {
    height: 20px;
    padding: 10px;
    position: relative;
    overflow: hidden;
    border: 1px solid #ffffff;
    transition: border-color 0.3s ease;
    background-color: transparent;
}

.link a {
    text-decoration: none;
    color: #fff;
}

.flex__links {
    display: flex;
    flex-direction: row;
    gap: 10px;
}

footer {
    width: 100%;
    height: 1012px;
    background-color: #282525;
}

.happy__new__year {
    display: flex;
    justify-content: end;
    position: relative;
    top: 42px;
    left: 30px;
}

.rotate {
    transition: transform 0.3s ease; /* Smooth transition for rotation */
    transform: rotate(180deg); /* Rotate icon when dropdown is open */
    
}

.checkpoint__ellipse {
    text-transform: uppercase;
    font-size: 14px;
    font-weight: inherit;
}

.checkpoint__ellipse:before {
    border-radius: 50%;
    content: "";
    display: inline-block;
    height: 8px;
    margin-right: 4px;
    width: 8px;
    background-color: #ffffff;
}

.hover__happy {
    transition: transform 0.3s ease; /* Smooth transition for the transform property */
}

.hover__happy:hover {
    transform: scale(1.1); /* Scale the image to 110% of its original size */
}

.checkpoint__ellipse {
    color: #ffffff;
}


#zapis {
    position: relative; /* For correct positioning of the pseudo-element */
    overflow: hidden; /* Hide overflow */
    border: 1px solid #000; /* Initial border color */
    padding: 10px 20px; /* Adjust padding as necessary */
    background-color: transparent; /* Ensure background is transparent */
    color: #000; /* Initial text color */
    font-size: 16px; /* Font size */
    cursor: pointer; /* Pointer cursor on hover */
    transition: color 0.3s ease; /* Smooth transition for text color */
    z-index: 1; /* Ensure button is above the pseudo-element */
}

#zapis::after {
    content: ''; /* Required for pseudo-element */
    position: absolute; /* Position it absolutely within the button */
    top: 0; /* Align to the top */
    left: 0; /* Align to the left */
    width: 100%; /* Full width of the button */
    height: 100%; /* Full height of the button */
    background-color: rgb(0, 0, 0); /* Color of the filling effect */
    transform: scaleX(0); /* Start with no scale (hidden) */
    transform-origin: left; /* Scale from the left side */
    transition: transform 0.3s ease; /* Smooth transition for scaling */
    z-index: -1; /* Place behind the button content */
    font-style: inherit;
}

#zapis:hover::after {
    transform: scaleX(1); /* Scale to full width on hover */
}

#zapis:hover {
    color: white; /* Change text color on hover for contrast */
}

.personal__presentation {
    font-size: 100px;
    color: #fff;
    text-transform: uppercase;
    white-space: nowrap;
    letter-spacing: -2.7px;
}

#name__field,
#number__field {
    width: 260px; /* Set width */
    height: 41px; /* Set height */
    border: none; /* Remove default border */
    border-bottom: 1px solid #fff; /* Underline effect */
    background-color: #282525; 
    color: #fff; /* Text color */
    font-size: 16px; /* Adjust font size as necessary */
    padding: 10px 0; /* Add padding for better spacing */
    outline: none; /* Remove outline on focus */
    transition: border-color 0.3s ease; /* Smooth transition for focus effect */
}

/* Focus effect */
#name__field:focus,
#number__field:focus {
    border-bottom: 1px solid rgba(243, 228, 20, 0.945);
}

#name__field:hover,
#number__field:hover {
    border-bottom: 1px solid rgba(243, 228, 20, 0.945);
}

#number__field, #name__field:focus {
    outline: none;
}

#number__field, #name__field {
    color: #ffffff66;
}

#listbox__btn {
    width: 260px; /* Set width */
    height: 41px; /* Set height */
    border: none; /* Remove default border */
    background-color: #282525; /* Background color */
    color: #ffffff66; /* Text color */
    font-size: 16px; /* Adjust font size as necessary */
    padding: 10px 0; /* Add padding for better spacing */
    outline: none; /* Remove outline on focus */
    border-bottom: 1px solid rgba(255, 255, 255, 0.959);
    cursor: pointer; /* Change cursor to pointer on hover */
    transition: border-color 0.3s ease, background-color 0.3s ease; /* Smooth transition for focus effect */
}

#listbox__btn:focus {
    border-bottom: 1px solid rgba(243, 228, 20, 0.945); /* Underline effect on focus */
}

::placeholder {
    color: #ffffff66; /* Text color */
}

.back__icon__foot {
    position: relative;
    left: 10px;
    top: 5px;
}

#zapis {
    width: 496px;
    height: 61px;
    background-color: #fdc300;
    color: black;
    border: none;
    cursor: pointer;
    text-align: center;
    
}

#copyright {
    color: #fff;
    text-decoration: underline;
}

.click {
    color: #fff;
    font-size: 14px;
}

.grid__container__fot {
    display: flex;
    flex-direction: column;

}

.center__footer {
    display: flex;
    justify-content: center;
    padding: 180px 0px 0px;
}

.input__row {
    display: flex;
    flex-direction: row;
    gap: 30px;
}

.tailw__first, .tailw__second {
    position: relative;
    top: -17px;
    left: -35px;
}

.btn__ta {
    padding-top: 21px;

}

.btn__cont__flex__footer {
    display: flex;
    justify-content: end;
    padding: 0px 0px 12px;
}

.copyrighting__fl {
    display: flex;
    justify-content: end;
}

.obertka__foote {
    position: relative;
    margin-top: -46px;
    width: 496px;
    margin-left: 1063px;
}

.custom-select {
  position: relative;
}

.dropdown {
  position: absolute;
  top: 100%; /* Position below the button */
  left: 0;
  background-color: #282525; /* Background color for dropdown */
  border: none; /* Border for dropdown */
  border-radius: 4px; /* Rounded corners */
  z-index: 10; /* Ensure dropdown is above other elements */
  color: #fff; /* Text color */
  
  /* Box shadow properties */
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
  
  width: 260px; /* Set a fixed width for the dropdown */
  max-height: 300px; /* Set a maximum height */
  overflow-y: auto; /* Enable vertical scrolling if content exceeds max height */
}

.dropdown ul {
  list-style: none; /* Remove bullet points */
  padding: 0; /* Remove padding */
  margin: 0; /* Remove margin */
}

.dropdown li {
  padding: 15px; /* Increase padding for each item */
  cursor: pointer; /* Pointer cursor on hover */
}

.dropdown li:hover {
  background-color: rgba(243, 228, 20, 0.1); /* Highlight on hover */
}

.dropdown ul {
  list-style: none; /* Remove bullet points */
  padding: 0;
  margin: 0;
}

.dropdown li {
  padding: 10px; /* Padding for dropdown items */
  cursor: pointer; /* Pointer cursor on hover */
}

.dropdown li:hover {
  background-color: rgba(243, 228, 20, 0.1); /* Highlight on hover */
}

.snowflake {
    position: absolute;
    top: -10px; /* Start above the container */
    background-color: white; /* Color of the snowflake */
    border-radius: 50%; /* Make it circular */
    pointer-events: none; /* Prevent interaction with snowflakes */
    box-shadow: 0 0 15px rgb(255, 255, 255), 0 0 10px white; 
}


</style>

<script>
export default {
  data() {
    return {
      isOpen: false,
      selectedOption: "Удобный способ связи", // Default selected option
      options: [
        "Email",
        "Телефон",
        "Чат",
        "Социальные сети"
      ],
      phoneNumber: "", // Data property for phone number
    };
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen; // Toggle dropdown visibility
    },
    selectOption(option) {
      this.selectedOption = option; // Set selected option
      this.isOpen = false; // Close dropdown
    },
    applyMask(event) {
      let input = event.target.value.replace(/\D/g, ''); // Remove non-digit characters

      // Limit to 11 digits for a Russian phone number (including +7)
      if (input.length > 11) {
        input = input.slice(0, 11);
      }

      // Format the value as a phone number
      let formattedValue = '';

      if (input.length > 0) {
        formattedValue += '+7 '; // Country code
      }
      if (input.length > 1) {
        formattedValue += `(${input.slice(1, 4)}) `; // Area code
      }
      if (input.length > 4) {
        formattedValue += `${input.slice(4, 7)}-`; // First part of the number
      }
      if (input.length > 7) {
        formattedValue += `${input.slice(7, 9)}-`; // Second part of the number
      }
      if (input.length > 9) {
        formattedValue += `${input.slice(9, 11)}`; // Last part of the number
      }

      // Set the formatted value back to the phoneNumber data property
      this.phoneNumber = formattedValue;

      // Update the input field directly to reflect the masked value
      event.target.value = formattedValue;
    },
    createSnowflake() {
      const container = this.$refs.snowContainer; // Use ref to get container

      if (!container) return; // Ensure the container exists

      const snowflake = document.createElement('div');
      snowflake.classList.add('snowflake');

      // Set random size for the snowflake (very small)
      const size = Math.random() * 5 + 2; // Random size between 2px and 7px
      snowflake.style.width = `${size}px`;
      snowflake.style.height = `${size}px`;

      // Set random position at the top of the container
      const leftPosition = Math.random() * container.offsetWidth;
      snowflake.style.left = `${leftPosition}px`;

      container.appendChild(snowflake);

      // Animate the falling effect
      const fallDuration = Math.random() * 3 + 2; // Random duration between 2s and 5s
      snowflake.style.transition = `transform ${fallDuration}s linear`;

      requestAnimationFrame(() => {
        snowflake.style.transform = `translateY(${container.offsetHeight + 20}px)`; // Fall down past the container
      });

      setTimeout(() => {
        snowflake.remove();
      }, fallDuration * 1000);
    },
    
    startSnowfall() {
        setInterval(this.createSnowflake, 300); // Create a new snowflake every 300ms
    }
  
},
  
mounted() {
   this.startSnowfall(); // Start snowfall when component is mounted 
}
};




</script>