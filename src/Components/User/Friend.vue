<template>
    <div class="user_friend">
            <h3>Friend information</h3>
        <ul>
            <li v-for="(friend,index) in friends" :key="index">
                {{index}} {{friend}}
            </li>
        </ul>
    </div>
</template>
<script>
    // import { bus } from '../../main.js';

    export default {
        data(){
            return{
                friends:['omo','pelz','precy','tkay','babs','oba','jimbo']
            }
        },
        // created() {
        //     bus.$on('addFriend',(value)=>{
        //         this.friends.push(value)
        //     })
        // }
    }
</script>

<style>
    .user_friend{
        border: 1px solid #2196f3;
        padding: 10px 20px;
    }
</style>