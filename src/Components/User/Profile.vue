<template>

        <div class="user_profile">
            <h3>User information</h3>
            <ul>
                <li><span>Name:</span> {{ userName }}</li>
                <li><span>Last name:</span> {{ lastName }}</li>
                <li><span>User Id:</span> {{ userId }}</li>
            </ul>
            <hr>
            <h3>Parent</h3>
            <ul>
                <li v-for="(value,def,index) in userParent" :key="index">
                    <span>{{def}}</span>
                        {{value}}
                </li>
            </ul>
            <button @click="updateName">Change</button>
            <button @click="updateLastName('Timi')">Change LN</button>
        </div>

    <div>
<!--        <input type="text" v-model="friendsName">-->
<!--        <button @click="addFriend">Add Friends</button>-->
    </div>

</template>
<script>
    // import { bus } from '../../main.js';
    export default {
        data(){
          return{
              friendsName:''
          }
        },
        props:{
            userName:String,
            lastName:String,
            userId:Number,
            userParent:Object,
            updateLastName:Function
        },
        methods:{
            updateName(){
                this.$emit('updateName','Frederick')
            },
            // addFriend(){
            //     alert('i was clicked');
            //     const name = this.friendsName;
            //     bus.$emit('addFriend', name);
            // }

        },
    }
</script>

<style>
    span{
        font-weight: 800;
    }
    .user_profile{
        border: 1px solid #2196f3;
        padding: 10px 20px;
    }
</style>