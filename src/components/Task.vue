<template>
<!-- we vbind/v-if the task.reminder here if its true it will add the 'reminder' class and we are saying we also want the task class, the css class are at the bottom  -->
  <div :class="[task.reminder ? 'reminder' : '', 'task' ]">
    <h3>
      {{ task.text }}
      <i @click="onDelete(task.id)" class="fas fa-trash"></i>
    </h3>
    <p>{{ task.day }}</p>
  </div>
</template>

<script>
export default {
  name: "TaskComponent",
  props: {
    task: Object,
  },
  methods:{
      onDelete(id){
          console.log(id)
      },
  },
};
</script>

<style scope>
.fas {
  color: red;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
