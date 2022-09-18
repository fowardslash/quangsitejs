<script>
    import Body from './components/Body.vue';
    import Topbar from './components/Topbar.vue'
    import Add from './components/Addition.vue'
    import Sidebar from './components/Sidebar.vue';
    export default{
        components: {
            Body,
            Topbar,
            Add,
            Sidebar,
        },
        data(){
            return {
                visible: true,
            }
        },
    }
</script>
<template>
    <Topbar></Topbar>
    <div :class="{XD : visible}">
        <div id="content">
            <Body></Body>
            <Add title="About me"></Add>
        </div>
        <Transition name="slide">
            <div id="sb" v-if="visible">
                <Sidebar @hidden="(n) => visible=n"></Sidebar>
            </div>
        </Transition>
    </div>
</template>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');
    @keyframes slide{
        from{
            opacity: 100%;
            transform: translate3d(0, 0, 0);
        }
        to{
            opacity: 0%;
            transform: translate3d(100px, 0, 0)
        }
    }
    .slide-enter-active,
    .slide-leave-active{
        animation: slide 0.5s cubic-bezier(.31,.17,0,1.04)
    }
    .XD{
        display: flex;
    }
    #sb{
        float: left;
        margin-left: auto;
    }
</style>