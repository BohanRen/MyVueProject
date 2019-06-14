<template>
    <div class="users">
        <ul>
            <li v-for="user in users" @click="user.show = !user.show">
                <h2 v-show="user.show">{{user.name}},{{user.position}}</h2>
            </li>
        </ul>
        <button @click="deleteUser()">删除一项</button>
    </div>
</template>

<script>
export default {
    name: 'Users',
    props:{
        users:{
            type:Array,
            required:true
        }
    },
    data(){
        return {
            
        }
    },
    methods:{
        deleteUser:function(){
            this.users.pop();
        }
    }
}
</script>

<style scoped>
    .users{
        width: 100%;
        max-width: 1200px;
        margin: 40px auto;
        padding: 0 20px;
        box-sizing: border-box;
    }
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        padding: 0;
    }
    li{
        flex-grow: 1;
        flex-basis: 200px;
        text-align: center;
        padding: 30px;
        border: 1px solid #222;
        margin: 10px;
    }
</style>