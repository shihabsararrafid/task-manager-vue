<template>
 <div :class="[task.reminder?'reminder':'',task]">
     <h3>{{task.text}}
     <p><i @click="deleteTask(task.id)" :style="{color:green}" class="fas fa-times"></i></p>
     </h3> 
  <h5>{{task.day}}</h5> 
 </div>
</template>

<script>
export default{
    name:'Task',
    props:{
        task:Object
    },
    methods:{
        deleteTask(id){
            this.$emit('delete-task',id);
            
        }
    }
}
</script>
<style scoped>
div{
    background-color: rgb(246, 243, 243);
    margin: 10px;
    padding: 10px;
    border-radius: 1px;
}
div h3{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
div .fas{
    color: red;
    font-weight: 700;
    font-size: larger;
    cursor: pointer;
}
.reminder{
    border-left: 4px solid green;

}
</style>