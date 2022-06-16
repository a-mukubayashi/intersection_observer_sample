<template>
  <div class="mozart-view">
    <div class="icons">
      <svg class="logo mozart" viewBox="50 25 298 338">
        <use xlink:href="/mozart.svg#icon" />
      </svg>
      <svg class="logo text" viewBox="0 15 391 32">
        <use xlink:href="/mozart-text.svg#icon" />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MozartView'
}
</script>

<style lang="scss" scoped>
.mozart-view {

.icons {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo {
  width: 200px;

  &.text {
    margin-top: 20px;
  }
}
// animation
@keyframes mozart_line {
  0% { stroke-dashoffset: 1750; }
  100% { stroke-dashoffset: 2000; }
}
@keyframes text_line {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
.mozart {
  stroke-dasharray: 500;
  stroke-dashoffset: 2000;
  stroke-width: 2;
  animation-name: mozart_line;
  animation-duration: 2.5s;
  animation-timing-function: ease-out;
}
.text {
  transform: translateY(-50px);
  animation-delay: 2.5s;
  opacity: 0;
  animation-fill-mode: forwards;
  animation-name: text_line;
  animation-duration: 2s;
  animation-timing-function: ease;
}
}
</style>
