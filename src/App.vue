<template>
  <HeaderComp header="Lucid Flashcard" />
  <FlashCardContainer :cards="cards"/>
  <FooterComp :url="readMoreUrl" />
</template>


<script>
import HeaderComp from './components/HeaderComp.vue';
import FlashCardContainer from './components/FlashCardContainer.vue';
import FooterComp from './components/FooterComp.vue';
import cards from './../data';

export default {
  name: 'App',
  components: {
    HeaderComp,
    FlashCardContainer,
    FooterComp,
  },
  data () {
    return {
      readMoreUrl: 'https://www.google.com',
      cards
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito&display=swap');


*{
  
  font-family: 'Nunito', sans-serif;
}
body{
  background-color: rgb(24,110,186);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}

</style>
