<script setup></script>
<template>
    <div class="days-tab text-center">
        <div class="loading">
            Loading.....
        </div>
        <ul class="p-0">
            <li class="li_active li-active-temp">
                <div class="py-3">icon</div>
                <div class="py-3">day</div>
                <div class="py-3">12oc</div>
            </li>
            <li class="li_active">
                <div class="py-3">icon</div>
                <div class="py-3">day</div>
                <div class="py-3">12oc</div>
            </li>
            <li class="li_active">
                <div class="py-3">icon</div>
                <div class="py-3">day</div>
                <div class="py-3">12oc</div>
            </li>
            <li class="li_active ">
                <div class="py-3">icon</div>
                <div class="py-3">day</div>
                <div class="py-3">12oc</div>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.days-tab {
    width: 90%;
    box-shadow: 0px 10px 60px 0px rgba(0, 0, 0, 0.2);
    border-radius: 20px;
    margin: auto;
}

.loading {
    color: aliceblue;
}

ul {
    margin: 0;
}

li {
    display: inline-block;
    list-style: none;
    height: 100%;
    width: 21%;
    max-width: 21%;
    font-size: 1vw;
    line-height: 1.2;
}

span {
    display: block;
    margin-bottom: 5px;
    font: 100% sans-serif;
    height: 35px;
}

.li_active {
    background-color: #203554;
    color: aliceblue;
    border-radius: 10px;
    margin: 0.5rem;
    font-weight: 600;
}

.li_active:hover {
    transform: scale(1.2);
    transition: transform 0.1s;
}

.li_acttive_temp {
    display: inline-block;
    background-color: #212730;
    color: aliceblue;
    transition: background-color 0.5s easy;
    border-radius: 10px;
}

.li_acttive_temp:hover {
    transform: scale(1.2);
    transition: transform 0.1s;
}
</style>
