<template>
  <a
    v-if="btnLink"
    class="v-btn v-btn__link"
    :class="className"
    :href="link"
  >
    {{title}}
  </a>
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
  },
  data () {
    return {}
  },
  mounted () {
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
  }
</style>
