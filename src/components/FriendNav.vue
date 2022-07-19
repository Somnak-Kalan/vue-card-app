<template>

  <li><a href=""> {{text}}</a></li>

</template>

<script>
export default {
    props:{
        text:String,
       
    }
}
</script>

<style>
ul{
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    justify-items: center;
    background: rgb(198, 24, 24);
}
ul li {
    list-style: none;
    margin: 10px;

    
}
ul li a{
    text-decoration: none;
    color: white ;
    font-weight: bold;
    font-size: 20px;
}
</style>