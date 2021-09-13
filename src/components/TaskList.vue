<template>
  <div class="single-task">
<span>
    {{ name }}
</span>
<span>
    {{description}}
</span>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    taskList: Array,
    name:String,
    description:String
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
.single-task{
    border: 1px solid black;
    width: 100px;
    height: 100px;
    display: flex;
    flex-direction: column;
    align-content: center;
    justify-content: center;
    padding: 30px;
}
</style>
