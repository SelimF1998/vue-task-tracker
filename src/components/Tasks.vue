<template>
    <div class="flex items-center justify-center" v-for="task in filteredList" :key="task.id">
      <Task @delete-task="$emit('delete-task', task.id)" :task="task" /> 
    </div>
</template>
<script>
import Task from "./Task.vue"

export default {
    name: "Tasks",
    props: {
        tasks: Array,
        filteredList: Array
    },
    components: {
      Task
    },
    emits: ['delete-task'],


    
}
</script>
<style>
    
</style>