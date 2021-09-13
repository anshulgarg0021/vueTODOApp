<template>
  <div id="app">
    <HelloWorld :msg=Title />
     <AddTaskInput :taskList=taskList :addTask="addTask"/>
     <ul>
      <li v-for="item in taskList" :key="item.id">
         <TaskList  :label="item.label" :name="item.name" :description="item.description" />
      </li>
    </ul>
    <button>Delete Task</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import AddTaskInput from "./components/AddTaskInput.vue";
import TaskList from "./components/TaskList.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    AddTaskInput,
    TaskList

  },
  data(){
    return {
      taskList: [{"name":"Dummy taks", "description":"Dummy taks description"}],
      Title:"Add New Tasks"
    }
  },
  methods:{
  addTask: function(name,description){
    console.log("aaaaa");
    this.taskList.push({"name":name,"description":description})
  }}
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
li{
  list-style-type: none;
  margin-right: 30px;
}
ul{
  display: flex;
  flex-wrap: wrap;
 ;
}
</style>
