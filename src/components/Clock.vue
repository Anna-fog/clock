<template>
  <div class="text">
    <img class="text__upper" alt="message" src="../assets/text.svg">
  </div>

  <div class="rectangle">

    <div class="rectangle__svg">
      <rectangles></rectangles>
    </div>

    <div class="counter">
      <img class="rectangle__timer" alt="rectangle" src="../assets/timer.svg">
<!--      {{ lifecycle }}-->
    </div>
  </div>
</template>

<script>

import Rectangles from "./Rectangles";
export default {

  data() {
    return {
      lifecycle: 2314742400,
    }
  },

  mounted() {
    const svg = this.$refs.svg;
    const list = Array.from(svg.querySelectorAll('rect'))
    list[0].classList.add('border-animation')
    list[0].classList.add('color-stroke-red')
  },

  components: {
    Rectangles
  }
}
</script>


<style lang="scss">
.text  {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &__upper  {
    display: block;
    animation: 86400s fadeOutText infinite;
  }
  &__lower  {
    display: block;
    margin-top: 5px;
  }
}

.rectangle {
  margin: 20px auto 0 auto;
  max-width: 680px;
  @media (max-width: 890px) {
    max-width: 338px;
  }
  @media (max-width: 320px) {
    max-width: 300px;
  }

  &__svg {
    max-width: 100%;
    @media (max-width: 890px) {
      max-width: 338px;
    }
    @media (max-width: 320px) {
      max-width: 300px;
    }
  }
}

.counter {
  text-align: right;
  text-shadow: 0 0 6px #FF003D;
  color: #FF003D;
}

.pulsing {
  animation: 1s ease-in-out pulse infinite;
}

.color-stroke-red {
  stroke: #FF003D;
}
.color-stroke-black {
  stroke: #12141C;
}

.border-animation {
  animation: 100s enlargeBorderWidth infinite;
}

@keyframes fadeOutText {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

@keyframes pulse {
  0% {
    opacity: 1
  }
  100% {
    opacity: 0
  }
}

@keyframes enlargeBorderWidth {
  0% {
    stroke-width: 1
  }
  100% {
    stroke-width: 680
  }
}

</style>