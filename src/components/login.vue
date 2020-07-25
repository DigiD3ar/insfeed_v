<template>
  <v-facebook-login app-id="{{ id }}"></v-facebook-login>
</template>

<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
    data() { 
    return { 
        id: process.env.fb_id
    }
}
  }
</script>