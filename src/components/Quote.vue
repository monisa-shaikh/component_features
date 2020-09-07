<template>
<div>
    <div>
    <slot name="title"></slot>
    </div>
       <div>
    <slot name="content"></slot>
       
    </div>
    <div><slot></slot></div>
    
</div>
</template>
<script>
export default {
    // props:['quote']
}
</script>
<style scoped>
div{
    border: 1px solid gray;
    box-shadow:1px 1px 2px black;
    padding: 30px;
    margin :30px auto;
    text-align: center;
}
h2{
    color:pink;
}
</style>