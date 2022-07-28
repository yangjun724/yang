<template>
<ul class="todo-main">
    <transition-group
    appear
    name="animate__animated animate__bounce"
    leave-active-class="animate__bounceOutRight"
    >
    <MyItem 
    v-for="todoObj in todos" :key="todoObj.id" 
    :todo="todoObj" 
    />
    </transition-group>
</ul>  
</template>

<script>
import 'animate.css'
import MyItem from './MyItem'
export default {
    name:'MyList',
    components:{MyItem},
    props:['todos',]
}

</script>

<style scoped>
  .todo-main {
    margin-left: 0px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
  }

  .todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
  }
</style>