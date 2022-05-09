<template>

<div>

  <Menu />
  <br>
  <div>Hello {{name}}</div>
  <button v-on:click="changeName" v-bind:disabled="btnState">Change</button>
  
  <!-- <p style="color:grey">   -->
  <!-- Write conditional inside html -->
    <!-- {{ btnState ? "The Button is disabled" : "Button works"}} -->
  <!-- </p> -->

  <br>
  <Skills />
  <br>

  

    <!-- Class Binding -->
    <!-- <div v-bind:class="alertObject"></div> -->

    <!-- Style Binding -->
    <!-- <div v-bind:style="{backgroundColor: bgcolor, width:bgwidth, height:bgheight}"></div> -->

  


  <!-- Using v-if -->
  <!-- <p v-if="skills.length>1"> You have more than 1 skill</p> -->
  <!-- <p v-else>You don't have enough skills</p> -->

</div>

</template>

<script>
import Menu from './components/Menu.vue'
import Skills from './components/Skills.vue'
import './components/Skills.css'

export default {
  name: 'App',
  components: {
    Menu,
    Skills,
    Skills
},
  data(){
    return {
      name: "Panos",
      btnState: true,
      // alertObject:
      // {
      //   alert:true,
      //   another:true,
      // },
      // bgcolor:'Green',
      // bgwidth:'120px',
      // bgheight:'60px',
    }
  }
}
 
</script>

<style>
* {
  margin: 0;
  padding: 0;
}



</style>
