<template>

    <div id="ninjas">
        <ul>
            <li v-for="ninja in ninjas" v-on:click="ninja.show =! ninja.show">
                <h2>{{ninja.name}}</h2>
                <h3 v-show="ninja.show">{{ninja.speciality}}</h3>
            </li>
        </ul>
    </div>

</template>

<script>
export default {
  data () {
    return {

      ninjas:[
          {name:'Julio', speciality:'Front-End', show:false},
          {name:'Vitor', speciality:'Back-End', show:false},
          {name:'Gabriel Fraga', speciality:'Alguma coisa', show:false},
          {name:'Gabriel Pioner', speciality:'Outra coisa', show:false},
          {name:'Mateus Winter', speciality:'Ser guei', show:false},
          {name:'Pessoa random', speciality:'Nada', show:false},
      ]
      
    }
  }
}

</script>

<style scoped>

#ninjas{

    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;

}
ul{

    display: flex;
    flex-wrap: wrap;
    list-style: none;
    padding: 0;
}
li{

    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;

}

</style>
