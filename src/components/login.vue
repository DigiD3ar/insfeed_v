<template>
  <v-facebook-login app-id=""></v-facebook-login>
</template>

<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
    mounted() {
  console.log(process.env.fb_id)
}
   
}
</script>