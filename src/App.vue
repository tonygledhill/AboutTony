<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import gsap from 'gsap';


//BeforeApperEvent
const beforeApperEvent = (el : any) => {
  el.style.opacity = 0;
  console.log("BeforeApperEvent");
}


//appearEvent
const appearEvent =() => {
  console.log("appearEvent");
}


//afterAppearEvent
const afterAppearEvent =() =>{
  console.log("afterAppearEvent");
}

//cancelledAppearEvent
const cancelledAppearEvent = () => {
  console.log("cancelledAppearEvent");
}


//beforeEnterEvent
const beforeEnterEvent = () => {
  console.log("beforeEnterEvent");
}

//enterEvent
const enterEvent = (el : any) =>{
  
// gsap.to(el, {
//   y:0,
//   opacity: 1,
//   //duration: 0.4

// })

}


//AfterEnterEvent
const afterEnterEvent = () => {
  console.log("AfterEnterEvent");
}

//CancelledEnterEvent
const cancelledEnterEvent = () => {
  console.log("cancelledEnterEvent");
}

//beforeLeaveEvent
const beforeLeaveEvent = () => {
  console.log("beforeLeaveEvent");
}

//leaveEvent
const leaveEvent = () => {
  console.log("leaveEvent");
}


//afterLeaveEvent
const afterLeaveEvent = () => {
  console.log("afterleaveevent");
}

//cancelledLeaveEvent
const cancelledLeaveEvent = () => {
  console.log("cancelledLeaveEvent");
}



</script>

<template>
  <header>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
  </header>
<!-- <Transition name="page" 

@before-appear="beforeApperEvent"
@appear="appearEvent"
@after-appear="afterAppearEvent"
@appear-cancelled="cancelledAppearEvent"

@before-enter="beforeEnterEvent"
@enter="enterEvent"
@after-enter="afterEnterEvent"
@enter-cancelled="cancelledEnterEvent"

@before-leave="beforeLeaveEvent"
@leave="leaveEvent"
@after-leave="afterLeaveEvent"
@leave-cancelled="cancelledLeaveEvent"

>   -->
  <RouterView />
<!-- </Transition> -->

</template>

<style scoped>

.page-enter-from{
opacity: 0;
transform: translatex(100vw);
}
.page-enter-to{
  opacity: 1;
  transform: translatex(0);
}
.page-enter-active{
  transition: all 0.4s ease;
}

</style>
