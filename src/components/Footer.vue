<template>
    <footer>
        <p>{{title}}</p>
        <p>{{copyright}}</p>
    </footer>
    <tt
</template>

<script>
export default {
    name: 'app-footer',
    props:{
        title:{
            type:String,
            required:true
        }
    },
    data (){
        return{
            copyright: "Copyright BobH@zendee.cn",
        }
    }
}
</script>

<style scoped>
    footer{
        background: #222;
        padding: 6px;
    }
    p{
        color: lightgreen;
        text-align: center;
    }
</style>