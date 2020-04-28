<template>
 <div>
   <label>
     <input type="text" v-model="login"/>
   </label>
   <label>
     <input type="text" v-model="password"/>
   </label>
     <button @click="register">register</button>
 </div>
</template>

<script>

  export default{
    name: 'Login',
    data () {
      return{
        login: '',
        password:''
        }
    },
    methods:{
      register() {
        this.$emit("register", {login: this.login,
                                            password: this.password})
      }

    }
  }

</script>

<style scoped>

</style>
