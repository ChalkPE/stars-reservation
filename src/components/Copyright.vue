<template>
  <span class="copyright">
    <a href="http://stars.kakaogame.com">팬메이드 페이지입니다</a>
    <a href="https://github.com/ChalkPE">(c) 2017-2018 ChalkPE</a>
    <a href="https://github.com/ChalkPE/stars-reservation/blob/master/LICENSE">Licensed under MIT</a>
    <a href="https://github.com/ChalkPE/stars-reservation">Fork on GitHub</a>
    <a @click="$emit('toggle')">{{ dark ? 'Light mode' : 'Dark mode' }}</a>
  </span>
</template>

<script>
  export default {
    name: 'Copyright',
    props: {
      dark: {
        type: Boolean,
        required: true
      }
    }
  }
</script>


<style lang="scss" scoped>
  .copyright {
    position: absolute;
    bottom: 0; right: 0; left: 0;

    opacity: 0.3;
    padding: 0.5vw;
    font-size: 14px;

    a + a:before {
      content: ' ★ ';
    }
  }
</style>
