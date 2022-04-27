<template>
    <div class="result">
        <p >ReactionTime : {{ score }} ms</p>
        <p class="rank">{{ rank }}</p>
    </div>
</template>

<script>
export default {
props: ['score'],
data(){
    return{
        rank:null
    }
},
mounted(){
    if(this.score < 250){
        this.rank = 'Ninja ringers'
    }
    else if(this.rank <400){
        this.rank = 'Rapid reflixes'
    }
    else{
        this.rank = 'snail pace ...'
    }
}
}
</script>

<style>
    .result{
        color: white;
        background: rgb(5, 230, 181);
        border: #444 1px;
        border-radius: 10px;
        width: 300px;
        text-align: center;
        padding: 50px 0;
        margin: 40px auto;
    }
    .rank{
        font-size: 1.4em;
        color: white;
        font-weight: bold;
    }
</style>