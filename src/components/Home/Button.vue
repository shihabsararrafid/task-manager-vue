<template>
    <button @click="onClick()" class="btn">Add task</button>
</template>


<script>


export default {
    name:'Button',
    methods:{
onClick(){
    console.log('clicked');
}
    }
       
}




</script>