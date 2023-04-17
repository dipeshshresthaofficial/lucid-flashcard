<template>
<div id="outer-div">
    <a :href="url">Read More</a>
    <p>&copy; Flashcard 2023</p>
</div>
</template>


<script>

export default{
    name: 'FooterComp',
    props: ['url'],
    components:{

    }
}
</script>

<style scoped>
#outer-div{
    margin-top: 20px;
    color: #fff;
}

#outer-div a{
    color: #fff;
}
</style>