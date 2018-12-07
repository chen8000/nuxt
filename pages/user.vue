<template>
  <section class="container">
    <div>
      <h1>这是父级</h1>
      <nuxt-link to="/user">user</nuxt-link>
      <input type="text" v-model="userId">
        <button @click="handleToDetail">跳转</button>

        <nuxt-child/>
    </div>
  </section>
</template>


<script>
export default {
    name:'User',
    data (){
        return{
            userId:""
        }
    },
    methods:{
        handleToDetail () {
            this.$router.push(`/user/${this.userId}`)
        }
    }
}
</script>


