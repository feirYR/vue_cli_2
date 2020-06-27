<template>
      <div>
        <p>第一页</p>
        <h3>1111111s</h3>
<!--        <router-link to="/c2?name=jim">组件2</router-link>-->
        <router-link to="/c2/jim/1">组件2</router-link>
        <button @click="go_c2">js跳转</button>
          <button @click="test_axios">测试axios</button>
          <button @click="test_vuex">测试vuex</button>
          <p>12121212121221</p>
      </div>

</template>

<script>
    export default {
      name: "c1",
      methods:{
        go_c2(){
          this.$router.push('c2/tom/3')
        },
        test_axios(){
            this.$axios({
                url:'http://127.0.0.1:8000/queryapp/test/',
                method:'get',
                params:{
                   'id':2
                }
            }).then(re=>{
                console.log('成功')
                this.$router.push('/c2')
            }).catch(error=>{
                console.log(error.data)
            })
        },
        test_vuex(){
            this.$store.commit('change_name','lucy')
        }
      }
    }
</script>

<style scoped>

</style>
