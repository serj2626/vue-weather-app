<script setup>
import { ref, onMounted, nextTick } from "vue";
import Weather from "./components/Weather.vue";

const city = ref("");
const showWeather = ref(false);

const searchWeather = async () => {
  showWeather.value = !false;
};
</script>

<template>
  <div class="app">
    <div class="header container h-100 p-5">
      <h1 class="mb-5">Погодное приложение</h1>
      <div class="d-flex justify-content-center h-100">
        <div class="searchbar mx-2 w-50">
          <input
            v-model="city"
            type="text"
            class="input form-control"
            placeholder="Введите город"
          />
        </div>
        <button @click="searchWeather" class="btn btn-search btn-primary">
          Поиск <i class="fas fa-search"></i>
        </button>
      </div>
    </div>
    <br />
    <Weather :city="city" v-if="showWeather"></Weather>
  </div>
</template>

<style></style>
