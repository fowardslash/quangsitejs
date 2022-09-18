<template>
    <div id="topbar">
        <div id="logo">
            <img src="../assets/qsIcon.png"/>
            <div id="txt">quang<b>SITE</b> | JS REWRITE</div>
        </div>
        <div id="links">
            <div id="entry">
                <a>HOME</a>
            </div>
            <div id="entry">
                <a>BLOG</a>
            </div>
            <div id="entry">
                <a>PROJECTS</a>
            </div>
            
        </div>
    </div>
</template>
<style>
    #entry{
        margin-left: 25px;
    }
    #links{
        display: flex;
        margin: auto 0 auto 0;
    }
    @import '../assets/var.css';
    #logo img{
        width: 48px;
        height: auto;
    }
    #txt{
        margin: auto 0 auto 0;
    }
    #logo{
        display: flex;
    }
    #topbar{
        display: flex;
        position: fixed;
        justify-content: space-around;
        top: 0;
        padding-top: 25px;
        padding-bottom: 25px;
        border: 2px var();
        width: 100%;
        padding-right: 250px;
        left: 0;
        border-bottom: 2px var(--bord) solid;
        background-color: var(--bg-o)
    }
</style>