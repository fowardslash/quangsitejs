<script>
    export default{
        data(){
            return{
                hidden: false,
            }
        },
        methods: {
            enable(){
                this.hidden=true;
                this.$emit('hidden');
            }
        }
    }
</script>
<template>
    <div id="sidebar">
        <div id="posts">
            <h2>LATEST POSTS</h2>
            <button class="material-symbols-outlined" id="closebt" @click="$emit('hidden')">close</button>
        </div>
        <div id="postframe">
            <img src="./icons/comingsoon.svg"/>
            <p>COMING SOON (I'M ONCE AGAIN LAZY.)</p>
        </div>
    </div>
</template>
<style>
    @import "https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0";
    @import '../assets/var.css';
    @keyframes rotate{
        from{
            transform: rotate(0deg)
        }
        to{
            transform: rotate(45deg)
        }
    }
    @keyframes rore{
        from{
            transform: rotate(45deg)
        }
        to{
            transform: rotate(0deg)
        }
    }
    #postframe img{
        display: block;
        margin-left: auto;
        margin-right: auto;
        filter: invert(75%);
        width: 64px;
        height: auto;
    }
    #postframe{
        margin: auto;
    }
    #postframe p{
        font-size: 20px;
        text-align: center;
    }
    #closebt{
        animation: rore 0.2s;
        margin: auto 0 auto 0;
        margin-left: auto;
        background: none;
        border: none;
        color: var(--txt)
    }
    #closebt:hover{
        animation: rotate 0.2s;
        transform: rotate(45deg)
    }
    #posts{
        display: flex;
    }
    #sidebar{
        border: 2px var(--bord) solid;
        margin-top: 250px;
        margin-bottom: 100px;
        min-height: 100%;
        width: 450px;
        margin-right: auto;
        border-radius: 16px;

    }
    #posts{
        margin-left: 25px;
        margin-right: 25px;
    }
</style>
