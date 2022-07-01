
<template>
    <div>
        <header :style="{display:flex}"   class="container ">
           <div class="newstyle">
             <h1>Task Tracker</h1>
            <Button  class="btn3"></Button>
           </div>
        </header>
    </div>
</template>
<script>
import Button from './Button.vue';
export default {
    name: "Header",
    components: { Button },
    
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
