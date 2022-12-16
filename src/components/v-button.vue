<template>
  <a
    v-if="btnLink"
    class="v-btn v-btn__link"
    :class="className"
    :href="link"
  >
    {{title}}
  </a>
  <button
    v-else-if="btnIco"
    class="v-btn v-btn__ico"
    :class="[btnIco, {'v-btn__sizem': sizeM }, {'v-btn__sizes': sizeS }]"
  >
  </button>
  <button
    v-else-if="btnTimer > 0"
    class="v-btn v-btn__classic v-btn__timer"
  >
    {{title}}<span>{{btnTimerLocalText}}</span>
  </button>
</template>

<script>
export default {
  name: 'v-btn',
  props: {
    title: {
      type: String,
      default: 'Button'
    },
    btnLink: {
      type: Boolean,
      default: false
    },
    link: {
      type: String,
      default: ''
    },
    btnIco: {
      type: String,
      default: ''
    },
    sizeS: {
      type: Boolean,
      default: false
    },
    sizeM: {
      type: Boolean,
      default: false
    },
    btnTimer: {
      type: Number,
      default: 0
    }
  },
  data () {
    return {
      btnTimerLocal: this.btnTimer,
      btnTimerLocalText: ''
    }
  },
  mounted () {
    let timerMin = 0
    let timerSec = 60
    const timerFunc = (count) => {
      this.btnTimerLocal--
      if (count) {
        if (this.btnTimerLocal > 59) {
          timerMin = Math.floor(this.btnTimerLocal / 60)
          if (timerMin > 99) {
            timerSec = (timerMin * 60) - 60
            this.btnTimerLocalText = timerMin + ':' + timerSec
          } else {
            timerSec = this.btnTimerLocal - (60 * timerMin)
            if (timerSec < 10) {
              timerSec = '0' + timerSec
            }
            if (timerMin < 10) {
              timerMin = '0' + timerMin
            }
            this.btnTimerLocalText = timerMin + ':' + timerSec
          }
        } else {
          if (this.btnTimerLocal < 10) {
            timerSec = '0' + this.btnTimerLocal
          } else {
            timerSec = this.btnTimerLocal
          }
          this.btnTimerLocalText = '00:' + timerSec
        }
        setTimeout(timerFunc, 1000, --count)
      }
    }
    timerFunc(this.btnTimerLocal)
  },
  computed: {
  },
  methods: {
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@700&display=swap');
</style>

<style lang="scss">
  .v-btn{
    font-size: 18px;
    padding: 0;
    border: none;
    text-align: center;
    color: #fff;
    cursor: pointer;
    &:focus{
      outline: none;
    }
    &__link{
      font-family: 'Nunito', sans-serif;
      text-decoration: underline;
      font-size: 16px;
      line-height: 18px;
      &:hover{
        color: #767679;
      }
      &:active{
        color: #C4296C;
      }
    }
    &__ico{
      background-position: center;
      background-repeat: no-repeat;
      border-radius: 18px 20px 18px 20px;
      &.v-btn__sizem{
        width: 60px;
        height: 60px;
      }
      &.v-btn__sizes{
        width: 52px;
        height: 52px;
        background-size: 24px;
      }
      &.ico__back{
        background-image: url('../assets/img/ico/back.svg');
        background-color: #702C7E;
      }
      &.ico__close{
        background-image: url('../assets/img/ico/close.svg');
        background-color: #DF3F3E;
      }
      &.ico__question{
        background-image: url('../assets/img/ico/quest.svg');
        background-color: #6DD1B0;
      }
      &.ico__next{
        background-image: url('../assets/img/ico/next.svg');
        background-color: #702C7E;
      }
      &.ico__gplus{
        background-image: url('../assets/img/ico/gplus.svg');
        background-color: #DF3F3E;
      }
      &.ico__vk{
        background-image: url('../assets/img/ico/vk.svg');
        background-color: #0083B6;
      }
      &.ico__ok{
        background-image: url('../assets/img/ico/class.svg');
        background-color: #ED732E;
      }
      &.ico__pencil{
        background-image: url('../assets/img/ico/pen.svg');
        background-color: #702C7E;
      }
    }
    &__timer{
      color: #767679;
      padding: 0 46px;
      span{
        background: #DF3F3E;
        line-height: 26px;
        color: #fff;
        margin-left: 6px;
        padding: 0 6px;
        border-radius: 8px 10px 8px 10px;
      }
    }
  }
</style>
