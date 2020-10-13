<template>
  <b-container>
    <b-row>
      <h1>{{ title }}</h1>  
    </b-row>
    <b-row>
      <div class="horas">
        <p> {{ parteDoDia() }} </p>      
      </div>
    </b-row>
  </b-container>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',
  components: {
  }, 
  data (){
    return {
      title: 'Locadora de filmes',
      horas: new Date().getHours()
    }
  },
  methods:{
    parteDoDia(){
      if(this.horas < 12){
        return "Esta de dia"
      }else if(this.horas >= 12 && this.horas < 18){
        return "Esta de tarde"
      }else if(this.horas >= 18){
        return "Esta de noite"
      }
    }
  }
}
</script>

<style>
  .row{
    justify-content: center;
  }

</style>
