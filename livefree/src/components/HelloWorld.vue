<template>
  <div class="hello">

          <div class="jumbotron">
              <h1 class="text-warning">Find Your Neighborhood</h1>
              <p class="text-warning">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
              <hr class="my-4">
              <p class="text-warning">It uses utility classes for typography and spacing to space content out within the larger container.</p>
              <p class="lead">
                <a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a>
              </p>
          </div>
          
          
          <div class="">
              <login/>
          </div>
          
          <br>
          
         <div class="row">
             <!-- looped later -->
              <rumah/> 
         </div>
            
          
      
  </div>
</template>

<script>
import rumah from './rumah'
import login from './login'
export default {

  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components : {
      rumah : rumah,
      login : login
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.jumbotron {
    background-image: url(../assets/pablo-vargas-17775.jpg);
    background-size: 100%;
    background-repeat: no-repeat;
    
}

.display-3{
    color: gray;
}
</style>
