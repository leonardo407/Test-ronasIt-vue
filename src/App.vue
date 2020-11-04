<template>
  <div id="app">
    <div class="container">
      <div class="header d-flex justify-content-between">

        <div>
          <h2>Омск</h2>

          <div class="d-flex align-items-center">
            <p class="opacity">Сменить город</p>

            <div class="header-location d-flex align-items-center">
              <img src="@/assets/img/location.svg" alt="">
              <p class="opacity">Мое местоположение</p>
            </div>
          </div>
        </div>

        <div class="d-flex align-items-start">
          <div class="d-flex align-items-center">
            <div class="header-point opacity">º</div>

            <div class="header-radio-wrapper d-flex">
              <div class="header-radio">
                <input
                    type="radio"
                    name="radio"
                    id="radio1"
                    checked
                />
                <label for="radio1">C</label>
              </div>

              <div class="header-radio">
                <input
                    type="radio"
                    name="radio"
                    id="radio2"
                />
                <label for="radio2">F</label>
              </div>
            </div>
          </div>
        </div>

      </div>

      <div class="middle d-flex align-items-center justify-content-center">
        <div>
          <div class="d-flex align-items-center">
            <img src="@/assets/img/cloudy.svg" alt="">
            <h1>19º</h1>
          </div>

          <h4 class="middle-description">Преимущественно солнечно</h4>
        </div>
      </div>

      <div class="footer">
        <div>
          <p class="opacity">Ветер</p>
          <h4 class="footer-value">5 м/c, западный</h4>
        </div>

        <div>
          <p class="opacity">Давление</p>
          <h4 class="footer-value">752 мм рт. ст.</h4>
        </div>

        <div>
          <p class="opacity">Влажность</p>
          <h4 class="footer-value">60%</h4>
        </div>

        <div>
          <p class="opacity">Вероятность дождя</p>
          <h4 class="footer-value">10%</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'App',
  }
</script>

<style lang="scss">
  #app {
    min-height: 100vh;
    background: $blue;
    border: 1px solid $grey;
    color: $white;
    font-size: 18px;
    line-height: 22px;
    font-family: 'Lato', sans-serif;
  }

  .header {
    margin-top: 75px;

    &-location {
      margin-left: 29px;
    }

    &-point {
      margin-right: 10px;
    }

    &-radio-wrapper {
      width: 77px;
      height: 29px;
      border: 1px solid $white;
      overflow: hidden;
      border-radius: 8px;
    }

    &-radio {
      width: 50%;
      height: 100%;
    }

    input[type='radio'] {
      display: none;
    }

    label {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      cursor: pointer;
      user-select: none;
      opacity: 0.4;
    }

    input[type='radio']:checked + label {
      background: rgba(255, 255, 255, 0.2);
      color: $white;
      opacity: 1;
    }
  }

  .middle {
    margin-top: 190px;

    &-description {
      margin-left: 40px;
    }
  }

  .footer {
    margin-top: 218px;
    margin-bottom: 122px;
    display: flex;
    justify-content: space-between;

    &-value {
      margin-top: 10px;
    }
  }
</style>
