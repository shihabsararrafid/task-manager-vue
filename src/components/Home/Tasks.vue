<template>
    <div :key="task.id" v-for="task in tasks">
        <Task @delete-task="deletedTask()" :task="task"></Task>
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
        deletedTask(){
            console.log('clicked from one level higher');
        }
    },
    components: { Task }
}
</script>