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
          <div class="wrap">
            <div class="wrap__line">
              <v-btn
                btnIco="ico__back"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__back"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__close"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__close"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__question"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__question"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__next"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__next"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__gplus"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__gplus"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__vk"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__vk"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__ok"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__ok"
                :sizeM="true"
              />
            </div>
            <div class="wrap__line">
              <v-btn
                btnIco="ico__pencil"
                :sizeS="true"
              />
              <v-btn
                btnIco="ico__pencil"
                :sizeM="true"
              />
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="wrap">
            <v-btn
              title="Повторное письмо"
              :btnTimer=240
            />
          </div>
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
