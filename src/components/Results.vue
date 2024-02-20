<template>
  <p v-if="showResults">Reaction time: {{score}} ms</p>
</template>

<script>
export default {
    setup(){
        let showResults = true
    
        props: [score]
    
    }
    

}
</script>

<style>

</style>