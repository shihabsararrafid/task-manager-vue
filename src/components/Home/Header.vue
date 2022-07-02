
<template>
    <div>
        <header tasks="tasks" :style="{display:flex}"   class="container ">
           <div class="newstyle">
             <h1>Task Tracker</h1>
            <Button  class="btn3"></Button>
           </div>
           <Tasks @delete-task="deletedTask" :tasks="tasks">
        
           </Tasks>
        </header>
    </div>
</template>
<script>
import Button from './Button.vue';
import Tasks from './Tasks.vue';
//let idnew ;
export default {
    name: "Header",
    components: { Button, Tasks },
    props:{
        tasks : Array
    },
    data(){
return{
    newId :[]
}
    },
    methods:{
        deletedTask(id){
            console.log(id);
            this.newId = id;
            this.$emit('deleted-task',id);
            console.log(this.newId);
            this.onClicked(this.newId);
        },
        onClicked(id){
            this.$emit('delete-task-new',id);
        }
    }
    
}
</script>
<style scoped>
.newstyle{
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 50px;
}
.btn3{
    height: auto;
}
</style>
