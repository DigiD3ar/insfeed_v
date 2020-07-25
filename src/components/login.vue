<template>
  <v-facebook-login :app-id="fb"></v-facebook-login>
</template>

<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
    data() { 
      return { 
          fb:process.env.fb
      }
    }
   
}
</script>