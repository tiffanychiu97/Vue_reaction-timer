<template>
  <div class="block" v-if="showBlock" @click="click">
    <p>Click me</p>
  </div>
</template>

<script>
import { shallowReactive } from 'vue'

export default {
    data(){
      return{
        showBlock: false,
        timer: null,
        reactionTime: 0 
      }
    },
    methods: {
      click(){
        this.showBlock = false;
        this.stopTimer()
      },
      startTimer(){
        this.timer = setInterval(() => {
          this.reactionTime+= 10
        }, 10)
      },
      stopTimer(){
        clearInterval(this.timer)
      }
    },
    props: ['delay'],
    OnMounted(){
      console.log('component mounted');
      setTimeout(() => {
        this.showBlock = true
        this.startTimer()
      }, this.delay)
    }
}
</script>

<style>
.block{
    width: 400px;
    background-color: burlywood;
    color: white;
    border-radius: 10px;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}

</style>