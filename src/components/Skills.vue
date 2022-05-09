<template>
    <div class="holder">
    <!-- create a form to use methods-->
    <form @submit.prevent="addSkill">
        <input v-model="skill" type="text" placeholder="Enter a skill you have">
    
    </form>
        <!-- display input -->
        <!-- {{skill}} -->
    <ul>
        <!-- Animations with animate.css -->
        <transition-group name="list" enter-active-class="animate__animated animate__backInUp" leave-active-class="animate__animated animate__bounceOut">
            <li v-for="(data,index) in skills" :key="index">
        <!-- {{ index }}  -->
             {{ data.skill }}
             <i class="bi bi-trash-fill" v-on:click="removeSkill(index)"></i>
            </li>
        </transition-group>
    </ul>
  </div>
  
</template>

<script>




export default {
    name:'Skills',
    data(){
        return {
        
        // skill i will write in input 
        skill:'',

        skills: [
        {skill:'Python'},
        {skill:'Django'},
        {skill:'Ruby'},
      ],
        }
    },
    methods: {
        addSkill(){
            this.skills.push({skill:this.skill})
            this.skill = ''
        },
        removeSkill(index){
            this.skills.splice(index,1)
        }

    }
}
</script>

<style>
    .holder {
        position: relative;
        background-color: white;
        width: 60vw;
        height: 300px;
        display: flex;
        justify-content: center;
        align-items: center;
    }


    .holder input {
        position: absolute;
        top: 0;
        border-radius: 20px;
        padding: 4px;
        display: flex;
        text-align: center;
        cursor: pointer;
        margin-left: 20px;
        
    }

    .holder ul {
        list-style-type: none;
    }

    .holder li {
        border: 1px solid black;
        border-radius: 10px;
        width: 200px;
        height: 30px;
        margin: 10px;
        display: flex;
        align-items: center;
        padding-left: 20px;
        background-color: aquamarine;
        position: relative;
    }

    .holder li i {
        position: absolute;
        right:10px;
        cursor: pointer;
    }
    
</style>