<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-2">
          <div class="wrap">
            <v-btn
              :btnLink="true"
              title="Напомнить PIN-код"
              link="https://animaccord.com/"
            />
            <v-btn
              :btnLink="true"
              title="Напомнить PIN-код"
              link="https://animaccord.com/"
            />
            <v-btn
              :btnLink="true"
              title="Напомнить PIN-код"
              link="https://animaccord.com/"
            />
          </div>
        </div>
        <div class="col-lg-2">
        </div>
        <div class="col-lg-4">
        </div>
        <div class="col-lg-4">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import vBtn from './components/v-button'

export default {
  name: 'App',
  components: {
    vBtn
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Phosphate Solid';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
