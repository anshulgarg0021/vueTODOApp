<template>
  <div class="hello">
   <input  v-model="taskName"/>
   <textarea  v-model="taskDescription"/>
   <button v-on:click="addTask(taskName,taskDescription)"> Add Task</button>
  </div>
</template>

<script>
export default {
  name: "AddTaskInput",
  props: {
    addTask: {type:Function},
  },
    data(){
    return {
     taskName:"",
      taskDescription:""
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
   background-color: #42b983;
}
h1{
    background-color: #42b983;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hello{
    display: flex;
    max-width: 400px;
    flex-direction: column;
    margin-left: auto;
    margin-right: auto;
}
</style>
