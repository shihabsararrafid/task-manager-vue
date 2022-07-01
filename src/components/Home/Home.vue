<template>
    <h1 >Hello {{msg}}</h1>
</template>

<script>

export default {
    name:'Home',
    props:{
        msg:String
    }
}

</script>
<style scoped>
h1{
    font-size:18px;
    font-weight: 500;
    color: rgb(61, 134, 134);
    font-size: 4rem;
    font-family: 'Times New Roman', Times, serif;

}
</style>