<template>
<div id="app">
  <navbar></navbar>
  <transition name="fade">
    <router-view></router-view>
  </transition>
  <foot></foot>
</div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Foot from '@/components/Footer'

export default {
  name: 'app',
  components: {
    Navbar,
    Foot
  }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity .5s
}

.fade-enter,
.fade-leave-to
/* .fade-leave-active below version 2.1.8 */

{
  opacity: 0
}
</style>
