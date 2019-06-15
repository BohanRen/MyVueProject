<template>
    <header @click="changeTitle()">
        <h1>{{title}}</h1>
    </header>
</template>

<script>
export default {
    name: 'app-header',
    props:{
        title:{
            type:String,
            required:true
        }
    },
    data (){
        return{

        }
    },
    methods:{
        changeTitle:function(){
            //this.title = "changed!!";
            this.$emit('titleChanged',"子向父组件传值");
        }
    },
    beforeCreate: function() {
        alert("组件实例化之前");
    },
    created: function() {
        alert("组件加载完毕，页面还没显示");
    },
    beforeMount() {
        alert("组件挂载前，页面还没展示，但虚拟dom已经生成");
    },
    mounted() {
        alert("组件挂载后，页面即将显示");
    },
    
}
</script>

<style scoped>
    header{
        background: lightgreen;
        padding: 10px;
    }
    h1{
        color: #222;
        text-align: center;
    }
</style>