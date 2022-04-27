<template>
    <header>
        <h1>{{title}}</h1>
        <Button 
        @toggle-add-task="$emit('toggle-add-task')" :text="showTaskFormBtns ? 'Close' : 'Add Task' " 
        :color="showTaskFormBtns ? 'red' : '#207567'  " />
    </header>
</template>

<script>
import Button from './Button.vue'
export default {
   name: 'HeaderComponent',
   props:{
       title:String,
       showTaskFormBtns: Boolean,
   },
   components:{
       Button
       }
}
</script>
<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        }
</style>