<script setup lang="ts">

</script>

<template>
  <div class="home">
    <img src="../assets/line/lines.svg">
    <div class="btn">进入</div>
  </div>
</template>

<style scoped>
.home {
  width: 100%;
  > img {
    width: 100%;
  }

  .btn {
    display: flex;
    align-items: center;
    justify-content: center;
    border: 0.266667vw solid #fff;
    background-color: #000;
    position: absolute;
    margin: auto;
    bottom: 32vw;
    width: 23.466667vw;
    height: 10.666667vw;
    z-index: 33;
    border-radius: 8vw;
    color: #fff;
    font-size: 5.333333vw;
    left: 0.8vw;
    right: 0;
    filter: drop-shadow(0 0 2.133333vw #767676);
    animation-name: shadows;
    animation-duration: 5s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: linear;
  }
}

@keyframes shadows {
  0% {
    filter: drop-shadow(0 0 2.133333vw #1e1e1e);
  }
  50% {
    filter: drop-shadow(0 0 2.133333vw #ffffff);
  }
  100% {
    filter: drop-shadow(0 0 2.133333vw #1e1e1e);
  }
}
</style>
