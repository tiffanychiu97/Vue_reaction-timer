<template>
  <div class="block">
    <p>Click me</p>
  </div>
</template>

<script>

export default {
    data(){
    
    },
    props: ['delay',]
}
</script>

<style>
.block{
    width: 400px;
    background-color: aquamarine;
    color: white;
    border-radius: 10px;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}

</style>