<template>
    <div  :key="task.id" v-for="task in tasks">
        <Task @toggle-Reminder="$emit('toggle-reminder',task.id)"  @delete-task="$emit('delete-task',task.id)" :task="task"></Task>
    </div>
</template>
<script>
import Task from './Task.vue';
 export default {
    name: "Tasks",
    props: {
        tasks: Array
    },
    methods:{
        deletedTask(id){
           this.$emit('delete-task-new',id);
        },
        toggleReminder(id){
            console.log(id);
        }
      
    },
    emits:['delete-task']
    ,
    components: { Task }
}
</script>