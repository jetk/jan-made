<template>
  <div id="app">
    <app-Navbar></app-Navbar>
    
    <router-view/>
  </div>
</template>

<script>
import appNavbar from '@/components/Navbar.vue'

export default {
  components : {appNavbar}
}
</script>


<style>
</style>
