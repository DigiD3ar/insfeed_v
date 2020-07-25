<template>
<div>

  <v-facebook-login :app-id="id ? id :''"
   v-model="model" @sdk-init="handleSdkInit" @login="login" ></v-facebook-login>
<span >{{ token != '' ?  token : "no token"}}</span>

</div>
</template>
<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
    data () {
        return {
          id: process.env.VUE_APP_FB,
          FB: {},
          model: {},
          scope: {},
          token:''
        }
    },
      methods:{
      handleSdkInit:function({ FB, scope }) {
        this.FB = FB
        this.scope = scope
      },
      login: function(x){
      this.token = x.authResponse.accessToken;
      }
 }
    
   
  }
</script>