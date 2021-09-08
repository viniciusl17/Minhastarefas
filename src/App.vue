<template>
  <header>Minhas Tarefas em Vue JS</header>
  <Task/>
</template>

<script>
import Task from './components/Task';
export default {
  name: 'App',
  components:{
    Task
  }
  
}
</script>

<style scoped>
header{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 80px;
  font-size: 30px;
  color: #fff;

}
</style>
