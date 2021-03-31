<template>
  <div class="text">
    <img class="text__upper" alt="message" src="../assets/text.svg">
  </div>

  <div class="rectangle">
    <img class="rectangle__svg" alt="rectangle" src="../assets/rectangle.svg">

    <div class="counter">
      <img class="rectangle__svg" alt="rectangle" src="../assets/timer.svg">
<!--      {{ lifecycle }}-->
    </div>
  </div>
</template>
<script>
export default {

  data() {
    return {
      lifecycle: 2314742400
    }
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

@keyframes fadeOutText {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

</style>