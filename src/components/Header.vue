<template>
<header>
<h1>{{title}}</h1>
<Button :text="showAddTask ? 'Close':'Add Task'" @btn-click="$emit('toggle-add-task')" :color="showAddTask ?'red':'green'"/>
</header>
</template>

<script>
import  Button from './Button';
export default{
    name:'Header',
    components:{
        Button

    },
    props:{
        title:String,
        showAddTask:Boolean
    }

}
</script>
<style scoped>
header {
    display: flex;
    justify-content:space-between;
    align-items: center;
    margin-bottom:20px;

}
</style>