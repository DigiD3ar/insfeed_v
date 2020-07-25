<template>
  <v-facebook-login :app-id="id ? id :''"></v-facebook-login>
</template>

<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
     data () {
       console.log(process.env.VUE_APP_FB)
        return {
          id: process.env.VUE_APP_FB,
        }
      }
    
   
  }
</script>