<script>
    export default{
        props: [
            'title',
            'subtitle'
        ],
    }
</script>
<template>
    <div id="main">
        <h1>{{title}}</h1>
        <p>{{subtitle}}</p>
    </div>
</template>
<style>
    @import '../assets/var.css';
    #main{
        border-top: 2px var(--bord) solid;
    }
    #main h1{
        text-transform: uppercase;
    }
</style>
