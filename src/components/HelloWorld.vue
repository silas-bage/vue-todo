<template>
<div>
  <div>
    <h4 class="bg-primary text-white text-center p-2">{{name}} 's' TODO List</h4>
  </div>
  <div class="container-fluid p-4">
    <div class="row mb-3">
      <div class="col font-weight-bold">
        Task
      </div>
        <div class="col-2 font-weight-bold">
        Done
      </div>
    </div>
    <div class="row" v-for="task in tasks" :key="task.action" >
      <div class="col">
         {{ task.action }}
      </div>
   
      <input type="checkbox" v-model="task.done" class="form-check-input"/>
      <div class="col-2">{{ task.done }}</div>
    </div>
  </div>
  </div>
</template>

<script>
export default {
   name: 'app',
   data () {
    return {
      name: 'Precious',
      tasks: [
        {action: 'Buy Flowers', done:false},
        {action: 'Call Joe', done:false},
        {action: 'Pick sister', done:false},
        {action: 'Read book', done:false},
      ]
    }
   }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
