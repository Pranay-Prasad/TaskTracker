
<template>
    <header>
        <h1>{{ title }}</h1>
        <Button  @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask?'Close':'Add Task'" :color = "showAddTask?'red':'green'" />
    </header>
</template>

<script>
import Button from './Button';
export default{
    name:'Header',
    props:{
        title:String,
        showAddTask: Boolean,
    },
    components:{
    Button,
    Button
}
}
</script>

<style scoped>
header{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
}
</style>