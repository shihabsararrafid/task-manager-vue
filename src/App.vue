

<script>
import Home from './components/Home/Home.vue'
import Header from './components/Home/Header.vue'
import Button from './components/Home/Button.vue'
import Tasks from './components/Home/Tasks.vue'

export default {
  components:{
    Home,
    Header,
    Button,
    Tasks
},
methods:{
  deletedTask(id){
    console.log("logging from app .vue app with the id",id)
  }
},
data(){
  return {
    tasks :[]
  }
}
,created(){
  this.tasks=[
    {
      id:1,
      text:'Join tfc 1 contest',
      day:'July 1 ,2022 at 3.00 pm ',
      reminder:true
    },
    {
      id:2,
      text:'Solve Problems from the marathon',
      day:'July 2,2022 at 8:00 am',
      reminder:false
    },
    {
      id:3,
      text:'Learn Vue js and create a new project',
      day:'July 3 ,2022 at 6:00 am',
      reminder:true
    }
  ]
}

}


</script>


<template>
  <header>
  
<Home msg="Rafid"></Home>
    <Header @delete-task-new="deletedTask" :tasks="tasks"></Header>
  
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
