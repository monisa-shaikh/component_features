<template>
<div>
   <h2>NEw</h2>  
   <button @click="counter++">counter</button>
   <p>{{ counter }}</p>
</div>
</template>
<script>
export default {
    // props:['quote']
    data:function(){
        return{
            counter:0
        };
    },
    destroyed(){
        console.log("destroyed components");
    },
    deactivated(){
        console.log("deactivated!!!");
    },
    activated(){
        console.log("Activated");
    }
}
</script>
<style scoped>

</style>