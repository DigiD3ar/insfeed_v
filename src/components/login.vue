<template>
  <v-facebook-login app-id=""></v-facebook-login>
</template>

<script>
  import VFacebookLogin from 'vue-facebook-login-component'

  export default {
    components: {
      VFacebookLogin
    },
    data() { 
    return { 
        id:process.env.fb_id, 
    }
},
    mounted() {
  console.log(this.id)
}
   
}
</script>