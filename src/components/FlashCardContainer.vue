<template>
  <div id="outer-container">
    <FlashCardComp :card="cards[cardIndex]"/>
    <div id="toggle-page-container">
        <button id="left" @click="changeIndex(-1)">&larr;</button>
        <button id="right" @click="changeIndex(1)">&rarr;</button>
    </div>
  </div>  
</template>

<script>

import FlashCardComp from './FlashCardComp.vue';

export default{
    name: 'FlashCardContainer',
    props: ['cards'],
    components: {
        FlashCardComp,
    },
    data(){
        return{
            cardIndex: 0,
        }
    },
    methods: {
        changeIndex(operator){
            if(this.cardIndex == 0 && operator == -1){
                alert('You are already viewing the first card item.');
            }else if(this.cardIndex == (this.cards.length - 1) && operator == 1){
                alert('You are already viewing the last card item.');
            }else{
                this.cardIndex = this.cardIndex + operator;
            }
        }
    }
}
</script>

<style scoped>
#outer-container{
    
}
#toggle-page-container{
    margin: 15px 0;
}

#toggle-page-container button{
    margin: 0 5px;
    font-size: 22px;
    font-weight: bolder;
    cursor: pointer;
    border-radius: 5px;
    border: none;
    color: rgb(24,110,186);
}
</style>