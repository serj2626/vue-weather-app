<script setup>
import DaysWeather from "./DaysWeather.vue";

defineProps({
  city: {
    type: String,
    default: "Moscow",
  }
})
</script>

<template>
  <div class="container p-0">
    <div class="d-flex">

      <div class="card main-div w-100">
        <div class="p-3">
          <h2 class="mb-1 day">Thursday</h2>
          <p class="text-light date mb-0">date</p>
          <small>time</small>
          <h2 class="place">
            <i class="fas fa-location">Rio <small>country</small></i>
            <div class="temp">
              <h1 class="weather-temp">19&deg</h1>
              <h2 class="text-light">description</h2>
            </div>
          </h2>
        </div>
      </div>

      <div class="card card-2 w-100">
        <table class="m-4">
          <tbody>
            <tr>
              <th>Humidity</th>
              <td>humidity</td>
            </tr>
            <tr>
              <th>Humidity</th>
              <td>humidity</td>
            </tr>
            <tr>
              <th>Humidity</th>
              <td>humidity</td>
            </tr>
          </tbody>
        </table>

        <DaysWeather />

        <div id="div_form" class="m-3 d-flex justify-content-center">
          <form action="">
            <input type="button" value="Change Location" class="btn btn-primary change-btn" />
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.weather-temp {
  margin: 0;
  font-size: 4rem;
  font-weight: 700;
}

h2.mb-1.day {
  margin: 0;
  font-size: 3rem;
  font-weight: 400;
}

.main-div {
  background: linear-gradient(90deg,
      rgba(2, 0, 36, 1) 0%,
      rgba(9, 9, 121, 1) 35%,
      rgba(0, 212, 255, 1) 100%);
  color: aliceblue;
  border-radius: 20px;
}

.temp {
  position: absolute;
  bottom: 0;
}

.main-div:hover {
  transform: scale(1.1);
  transition: 0.9s;
  z-index: 1;
}

.card-2 {
  background-color: #212730;
  color: aliceblue;
  border-radius: 20px;
}

.card-details {
  margin-left: 19px;
}

.h1_left {
  position: absolute;
  bottom: 25px;
  left: 16px;
  font-size: 3vw;
  line-height: 1.2;
}

.h3_left {
  position: absolute;
  left: 16px;
  font-size: 2vw;
  line-height: 0.5;
}

.h3_left small {
  font-size: 1rem;
}

table {
  position: relative;
  left: 15px;
  border-collapse: separate;
  border-spacing: 15px;
  width: 85%;
  text-align: left;
}

th,
td {
  font-size: 18px;
  color: white;
}

td {
  text-align: right;
}

table,
tr:hover {
  color: red;
}

.change-btn {
  background: linear-gradient(to right, #00b09b, #96c93d);
}

.change-btn:hover {
  transform: scale(0.9);
  transition: 0.1s ease;
}
</style>
