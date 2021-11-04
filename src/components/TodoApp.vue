<template>
    <div>
        <h1>{{ msg }}</h1>
        <input v-model="task"/>
        <button v-on:click="submitTask">Submit</button>
        <div v-show="isShowHideText">
            <p>Helloworld</p>
        </div>
       
        <div v-for="(task, index) in tasks" :key="index">
          <td>{{task.name}}</td>
          <td>{{task.status}}</td>
          <td @click="deleteTask">x</td>
          <td ></td>
        </div>
    </div>
</template>

<script>
export default {
  name: 'TodoApp',
  props: {
    msg: String
  },
  data(){
    return {
      isShowHideText: true,
      task:'',
      tasks: [
        {
          name: 'Hello world 1',
          status: 'to-do'
        },
          {
          name: 'Hello world 1',
          status: 'in-progress'
        }
      ]
    }
  },
  methods: {
    submitTask(){
      if(this.task.length === 0) return ;
      this.tasks.push({
        name:this.task,
        status: 'to-do'
      })
      this.task = ''
    },
    deleteTask(index){
      this.tasks.splice(index, 1)
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
