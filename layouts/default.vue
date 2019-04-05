<template>
  <div>
    <TheHeader @sidenavToggle="diplaySideNav=!diplaySideNav"/>
    <TheSidenav 
    :show="diplaySideNav"
    @close="diplaySideNav = false"  />
    <nuxt />
  </div>
</template>

<script>
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
export default {
  components : {
    TheHeader,
    TheSidenav 
  },
  data(){
    return {
      diplaySideNav : false
    }
  }  
}
</script>


<style>
html {
  font-family: 'Open Sans', sans-serif;
}
body {
  margin: 0;
}
</style>
