<template>
  <div id="app">
    <app-header @titleChanged="updateTitle($event)" v-bind:title="title"></app-header>
    <users v-bind:users="users"></users>
    <users v-bind:users="users"></users>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  name: 'App',
  methods:{
    updateTitle:function(val){
      this.title = val;
    }
  },
  data(){
    return{
      title:"Vue.js Demo",
      users:[
                {
                    name:"刘青文",
                    position:"信息科主任",
                    show:true,
                },
                {
                    name:"王键",
                    position:"信息学教练",
                    show:true,
                },
                {
                    name:"李正平",
                    position:"计算机教师",
                    show:false,
                },
                {
                    name:"周逸松",
                    position:"划水睡觉员",
                    show:true,
                }
      ],
      title:"传递的是值"
    }
  },
  components:{
    "users":Users,
    "app-header":Header,
    "app-footer":Footer,
  }
}

</script>

<style scoped>
  h1{
    color:red;
  }
</style>
