<template>
    <div>
      <p>第二页</p>
<!--      <span>{{$route.query.name}}</span>-->
      <span>{{$route.params.name}},{{$route.params.id}}</span><br>
      <span>S:{{$store.state.name}}</span><br>
        <span>g:{{$store.getters.new_name}}</span>
        <span>br1第二次修改</span>
    </div>
</template>

<script>
    export default {
        name: "c2"
    }
</script>

<style scoped>

</style>
