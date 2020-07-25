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
        return {
          id: process.env.VUE_APP_FB,
        }
    },
     methods: {
      connected({ res }) {
       console.log(res)
      }
    }
    
   
  }
</script>