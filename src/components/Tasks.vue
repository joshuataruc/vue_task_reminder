<template>
    <div :key="task.id" v-for="task in tasks">
        <!-- we are getting the @delete-task event from the task.vue with the task.id and  we are gonna pass it on the App.vue because our array is there -->
        <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
    </div>
</template>
<script>
import Task from './Task'
export default{
    name:'TasksComponent',
    props:{
        tasks:Array
    },
    components:{
        Task,
    },
     // we got the delete-task from the @delete-task
     emits: ['delete-task'],
}
</script>
