<template>
    <button @click="OnClick()" class="btn" :style="{background: color }" >{{text}} </button>
</template>

<script>
export default {
        name:'ButtonComponent',
        props:{
            text:String,
            color:String,
        },
        methods:{
            OnClick(){
               this.$emit('toggle-add-task')
            }
        }
}
</script>