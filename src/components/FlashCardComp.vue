<template>
    <div id="flash-card" @click="isFlipped = !isFlipped">
        <p v-if="!isFlipped" v-text="card.front"></p>
        <p v-else v-html="card.back"></p>
    </div>
</template>

<script>

export default{
    name: 'FlashCardComp',
    props: ['card'],
    data(){
        return{
            isFlipped: false,
        }
    }
}
</script>

<style scoped>

#flash-card{
    min-height: 300px;
    min-width: 400px;
    width: 600px;
    /* border: 2px solid #000; */
    margin: 0 auto;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 10px;
    background-color: #fff;
    box-shadow: 4px 5px 30px -9px rgba(5, 0, 0, 0.64);
    font-size: 18px;
    font-weight: 700;
    color: rgb(24,110,186);
    padding: 20px;
}

#flash-card p{
    
}
</style>