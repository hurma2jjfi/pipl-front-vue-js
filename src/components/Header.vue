<template>
    <header class="header">
        <div class="header__grid__wrapper">
            <svg width="76" height="46" viewBox="0 0 76 46" fill="none" xmlns="http://www.w3.org/2000/svg" 
            class="mr-[39.3%] h-[36px] cursor-pointer lg:mr-0 lg:h-full delay-1000" data-v-aec9a781="">
            <path d="M0 13.4922H20.9236V16.5749H18.4721V35.1273H14.9373V16.5749H6.04334V35.1273H2.50856V16.5749H0V13.4922Z" fill="black"></path>
            <path d="M20.9844 18.0874H24.5192V32.0998L35.6936 21.058V18.0874H39.2284V39.7225H35.6936V25.4299L24.5192 36.4156V39.7225H20.9844V18.0874Z" fill="black">
            </path>
            <path d="M39.2758 13.4917H60.1994V16.5744H57.7479V35.1268H54.2131V16.5744H45.2621V35.1268H41.7273V16.5744H39.2188V13.4917H39.2758Z" fill="black"></path>
            <path d="M60.2619 18.0874H75.0282V31.0349V45.1594H71.3223V21.2262H63.9677V23.7484C63.9677 31.147 63.6256 36.808 62.4854 40.283C61.1171 44.2626 58.4945 46.0001 55.0738 46.0001C53.3064 46.0001 51.824 45.3836 50.6268 44.2065C49.8286 43.4218 49.6005 42.8053 48.8594 41.348L51.881 38.7137C52.8503 41.2919 54.2186 42.3008 55.5869 42.3008C58.4945 42.3008 60.2049 35.7991 60.2049 23.8045V18.0874H60.2619Z" fill="#FDC300"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M67.734 3.44385C65.3196 3.44385 63.4126 5.36045 63.4126 7.66318C63.4126 9.96592 65.3196 11.8825 67.734 11.8825C70.1484 11.8825 72.0554 9.96592 72.0554 7.66318C72.0554 5.36045 70.1484 3.44385 67.734 3.44385ZM59.9688 7.66318C59.9688 3.40339 63.4732 0 67.734 0C71.9949 0 75.4993
             3.40339 75.4993 7.66318C75.4993 11.923 71.9949 15.3264 67.734 15.3264C63.4732 15.3264 59.9688 11.923 59.9688 7.66318Z" fill="#FDC300">
            </path></svg>
            <div class="flex__items__links">
            <div class="hidden__call">
                <button class="btn__call">Заказать звонок</button>
            </div>
            <div class="select__kvart">
                <button class="slct__kvar">Выбрать квартиру</button>
            </div>
            <span class="tailwind-svg-icon text-black text-[22px]"><svg width="22" height="23" viewBox="0 0 22 23" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect y="0.375" width="22" height="22" rx="4" fill="#FDC300"></rect>
<path d="M12.5332 10.2251L16.0337 13.6751L12.5332 17.1251" stroke="currentColor"></path>
<path d="M15.9325 13.675H8.96582C7.30897 13.675 5.96582 12.3319 5.96582 10.675V5.625" stroke="currentColor"></path>
</svg>
</span>
            </div>
            <div class="burger__btn">

            </div>
        </div>
    </header>
</template>


<style>


header {
    width: 100%;
    height: 50px;
    padding: 12px 40px;
    background-color: #F1F1ED;
    display: flex; /* Добавляем flex для header */
    justify-content: center; /* Центрируем содержимое */
}

.header__grid__wrapper {
    display: flex;
    justify-content: space-between; /* Содержимое внутри блока будет распределено */
    width: 100%; /* Занимает всю ширину родителя */
}

.flex__items__links {
    display: grid;
    justify-content: space-evenly;
    align-content: space-between;
    align-items: center;
    justify-items: start;
    display: flex;
    gap: 20px;
 
}

.slct__kvar {
    background-color: #F1F1ED;
    border: none;
    text-decoration: underline;
    cursor: pointer;
    text-underline-offset: 4px;
}

.btn__call {
    border: none;
    background-color: #F1F1ED;
    cursor: pointer;
}

.flex__svg {
    display: flex;
    justify-content: end;
    position: relative;
    top: -22px;
}

</style>

<script>

</script>