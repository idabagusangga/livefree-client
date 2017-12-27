<template>
  <div class="hello">
        
          <div class="jumbotron">
              <h1 class="text-warning">C A S T L E  H U N T E R</h1>
              <p class="text-warning">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
              <hr class="my-4">
              <p class="text-warning">It uses utility classes for typography and spacing to space content out within the larger container.</p>
              <p class="lead">
                <a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a>
              </p>
          </div>
          
          <div class="container">
              <div>
                  <login/>
                  
              </div>
              <br>
              
              <div class="">
                  <FBlogin/>
              </div>
          </div>
          
          
          <br>
          
         <div class="row">
              <rumah v-for="h in houses" :house='h'/> 
         </div>
          
      
  </div>
</template>

<script>
import rumah from './rumah'
import login from './login'
import facebook from './facebook'
import axios from 'axios'
export default {

  name: 'HelloWorld',
  data () {
    return {
      houses    : []
    }
  },
  components : {
      rumah : rumah,
      login : login,
      FBlogin:facebook
  },
  mounted: function(){
    this.getHouses()  
  },
  methods   : {
      getHouses(){
          axios.get('http://localhost:3000/api/house') //test without token
          .then(response=>{
              this.houses = response.data.houses
          })
          .catch(err=>{
              console.log(err);
          })
      }
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
