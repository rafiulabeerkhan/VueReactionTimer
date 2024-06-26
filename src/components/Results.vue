<template>
  <p>Reaction Time - {{ score }} Milliseconds</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
props:['score'],
data(){
    return {
        rank:null
    }
},
mounted(){
    if (this.score < 250 ){
        this.rank = "Ninja Fingers"
    } else if(this.score < 400){
        this.rank = 'Rapid Reflexes'
    } else{
        this.rank = "Snail Pace.."
    }
}
}
</script>

<style>
.rank{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-size: larger;
    color: brown;
    font-weight: bolder;
}
</style>