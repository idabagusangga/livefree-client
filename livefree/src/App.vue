<template>
    <div class="">
        <navtop/>
        <div id="app">
            
          <router-view/>
        </div>    
    </div>
  
</template>

<script>
import header from '@/components/header'
export default {
  name: 'app',
  components : {
      navtop : header
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
