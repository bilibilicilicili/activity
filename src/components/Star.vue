
<template>
  <div class="home">
    <img class="stars" src="../assets/star/stars.png">
    <div class="star star1"></div>
    <div class="star star2"></div>
    <div class="star star3"></div>
    <div class="star star4"></div>
    <img class="meteor meteor1" src="../assets/star/meteor.png">
    <img class="meteor meteor2" src="../assets/star/meteor.png">
    <img class="meteor meteor3" src="../assets/star/meteor.png">
    <img class="meteor meteor4" src="../assets/star/meteor.png">
    <img class="meteor meteor5" src="../assets/star/meteor.png">
    <img class="meteor meteor6" src="../assets/star/meteor.png">
    <img class="meteor meteor7" src="../assets/star/meteor.png">
    <img class="meteor meteor8" src="../assets/star/meteor.png">
    <img class="meteor meteor9" src="../assets/star/meteor.png">
    <img class="meteor meteor10" src="../assets/star/meteor.png">
    <img class="meteor meteor11" src="../assets/star/meteor.png">
    <img class="meteor meteor12" src="../assets/star/meteor.png">
    <img class="meteor meteor13" src="../assets/star/meteor.png">
    <img class="meteor meteor14" src="../assets/star/meteor.png">
    <img class="meteor meteor15" src="../assets/star/meteor.png">
    <img class="meteor meteor16" src="../assets/star/meteor.png">
    <img class="meteor meteor17" src="../assets/star/meteor.png">
    <img class="meteor meteor18" src="../assets/star/meteor.png">
    <img class="meteor meteor19" src="../assets/star/meteor.png">
    <img class="meteor meteor20" src="../assets/star/meteor.png">

    <div class="alien-container">
      <div class="galaxy"></div>
      <div class="light"></div>
      <div class="ship">
        <div class="belt"></div>
      </div>
      
    </div>
  </div>
</template>
<script setup lang="ts">
import { gsap } from 'gsap';
window.onload = function() {
  const line = gsap.timeline();

  line.to('.meteor', { x: -1000, y: 1000, duration: 10,  repeat: -1},'+=1')
  
  // gsap.to(".meteor", {rotation: 270, x: 1000, duration: 10, repeat: -1, yoyo: false, onComplete:()=>{
  //   console.info(1111)
  // }})
}


</script>

<style scoped>
.home {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  background-image: url('../assets/star/bg.png');
  background-position: center center;
  background-repeat: no-repeat;
  background-size: auto 100%;
  > img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
  }

  .star {
    position: absolute;
  }

  .star1 {
    top: -20px;
    left: -30px;
    width: 330px;
    height: 330px;
    background-image: url('../assets/star/star1.png');
    transform: scale(0);
    animation-name: track1;
    animation-duration: 15s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: linear;
  }

  .star2 {
    top: 0px;
    left: 120px;
    width: 323px;
    height: 329px;
    background-image: url('../assets/star/star2.png');
    transform: scale(0);
    animation-name: track2;
    animation-duration: 15s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: linear;
    transition-delay: 8s;
  }
/* 
  .star3 {
    top: -100px;
    left: -100px;
    width: 428px;
    height: 428px;
    background-image: url('../assets/star/star3.png');
    transform: scale(0);
    animation-name: track3;
    animation-duration: 15s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: linear;
    transition-delay: 8s;
  } */

  .alien-container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0.5);
    width: 290px;
    height: 290px;
  }

  .galaxy {
    width: 290px;
    height: 290px;
    background-image: url('../assets/star/photo.png');
    background-position: 507px 484px;
    animation-name: rotation;
    animation-duration: 2.5s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: linear;
  }
  .ship {
    position: absolute;
    top: 45%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 281px;
    height: 119px;
    background-image: url('../assets/star/photo.png');
    background-position: 2032px 294px;
    animation-name: shake;
    animation-duration: 2.5s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: ease-in-out;
  }

  .belt {
    position: absolute;
    top: 25px;
    left: -9px;
    width: 300px;
    height: 52px;
    background-image: url('../assets/star/photo.png');
    background-position: 524px 181px;
    animation-name: light;
    animation-duration: 0.8s;
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: ease-in-out;
    opacity: 0.3;
  }

  .light {
    position: absolute;
    top: 200px;
    left: 143px;
    width: 64px;
    height: 101px;
    background-image: url('../assets/star/photo.png');
    background-position: 1589px 166px;
    animation-name: shake, light;
    animation-duration: 2.5s, 0.8s;
    /* animation-delay: 0.1s; */
    animation-iteration-count: infinite;
    animation-fill-mode: both;
    animation-timing-function: ease-in-out;
    opacity: 0.3;
  }

  .meteor {
    position: absolute;
  }

  .meteor1 {
    top: -200px;
    left: 100px;
    transform: scale(0.1) rotate(-10deg);
  }

  .meteor2 {
    top: -100px;
    left: 400px;
    transform: scale(0.15) rotate(-10deg);
  }

  .meteor3 {
    top: 100px;
    left: 500px;
    transform: scale(0.13) rotate(-10deg);
  }

  .meteor3 {
    top: -200px;
    left: -8px;
    transform: scale(0.09) rotate(-10deg);
  }

  .meteor4 {
    top: 200px;
    left: 800px;
    transform: scale(0.09) rotate(-10deg);
  }

  .meteor5 {
    top: 200px;
    left: 250px;
    transform: scale(0.12) rotate(-10deg);
  }

  .meteor6 {
    top: 350px;
    left: 800px;
    transform: scale(0.11) rotate(-10deg);
  }

  .meteor7 {
    top: 400px;
    left: 400px;
    transform: scale(0.1) rotate(-10deg);
  }

  .meteor8 {
    top: 200px;
    left: 800px;
    transform: scale(0.09) rotate(-10deg);
  }

  .meteor9 {
    top: 300px;
    left: 900px;
    transform: scale(0.12) rotate(-10deg);
  }

  .meteor10 {
    top: 100px;
    left: 300px;
    transform: scale(0.09) rotate(-10deg);
  }

  .meteor11 {
    top: 20px;
    left: 600px;
    transform: scale(0.13) rotate(-10deg);
  }

  .meteor12 {
    top: 500px;
    left: 500px;
    transform: scale(0.1) rotate(-10deg);
  }

  .meteor13 {
    top: 350px;
    left: 500px;
    transform: scale(0.1) rotate(-10deg);
  }

  .meteor14 {
    top: 400px;
    left: 600px;
    transform: scale(0.125) rotate(-10deg);
  }

  .meteor15 {
    top: -40px;
    left: 600px;
    transform: scale(0.125) rotate(-10deg);
  }

  .meteor16 {
    top: 100px;
    left: 1200px;
    transform: scale(0.125) rotate(-10deg);
  }

  .meteor17 {
    top: 350px;
    left: 600px;
    transform: scale(0.125) rotate(-10deg);
  }


  .meteor18 {
    top: 200px;
    left: 400px;
    transform: scale(0.125) rotate(-10deg);
  }

  .meteor19 {
    top: 50px;
    left: 700px;
    transform: scale(0.125) rotate(-10deg);
  }

  .meteor20 {
    top: -200px;
    left: 120px;
    transform: scale(0.12) rotate(-10deg);
  }

}

@keyframes rotation {
  0% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(180deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@keyframes shake {
  0% {
    transform: translate(-50%, -50%);
  }
  50% {
    transform: translate(-50%, calc(-50% - 20px));
  }
  100% {
    transform: translate(-50%, -50%);
  }
}

@keyframes light {
  0% {
    opacity: 0.3;
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0.3;
  }
}

@keyframes track1 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(0.8) translate(-3000px, -1500px);
  }
}


@keyframes track2 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1) translate(3000px, -2000px);
  }
}


/* @keyframes track3 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(0.7) translate(-4000px, -2000px);
  }
} */
</style>
