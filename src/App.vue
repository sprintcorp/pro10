<template>
  <div>
    <app-header></app-header>
    <div class="container">
      <comp-user :userName="name"
                 :userId="id"
                 :lastName="lastname"
                 :userParent="parent"
                 @updateName="name = $event"
                 :updateLastName="updateLastName"
      ></comp-user>
      <comp-friend/>
    </div>

    <compFooter/>
  </div>
</template>

<script>
  import compFooter from './Components/Header_footer/Footer.vue';
  import compUser from './Components/User/Profile.vue';
  import compFriend from './Components/User/Friend.vue';
export default {
  data () {
    return {
      name: 'Sprintcorp',
        lastname: 'Ade',
        id: 1,
        parent:{
          mother:'Jill',
          father: 'Jack'
        }
    }
  },
    methods:{
        updateLastName(value){
            this.lastname = value
        }
    },

  components:{
    compFooter,
    compUser,
    compFriend
  }
}
</script>

<style>
body{
    padding:0;
    margin: 0;
    font-family: 'Roboto', sans-serif;
}
    .container{
        min-height: 84vh;
        box-sizing: border-box;
        padding: 20px;
    }
</style>
