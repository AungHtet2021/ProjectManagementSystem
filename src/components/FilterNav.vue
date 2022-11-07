
<template>
    <nav class="Filter-nav">
        <button @click="filterBy('all')" :class="{active:current==='all'}">All</button>
        <button @click="filterBy('complete')" :class="{active:current==='complete'}">Complete</button>
        <button @click="filterBy('ongoing')" :class="{active:current==='ongoing'}">Ongoing</button>
    </nav>
</template>

<script>
    export default{
        props:['current'],
        methods:{
            filterBy(value){
                this.$emit('filterValue',value)
            }
        }
    }
</script>

<style >
    .Filter-nav button{
        background: none;
        border:none;
        color:#bbb;
        outline:none;
        font-size:12px;
        text-transform: uppercase;
        margin-right: 10px;
        letter-spacing: 1px;
        font-weight: bold;
        cursor:pointer;
    }
   button.active{
        color:#333;
    }
</style>