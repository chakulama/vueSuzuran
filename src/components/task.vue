<template>
 <div class='ui centered card'>
    <div class='content'>
        <div class='header'>
            {{ task.name }}
        </div>
        <div class='meta'>
            {{ task.Title }}
        </div>
        <div class='extra content'>
            <span class='right floated edit icon'>
            <i class='edit icon'></i>
          </span>
        </div>
    </div>
    <div class='ui bottom attached green basic button' v-show="task.done" @click="Incompleted(task)">
        Completed
    </div>
    <div class='ui bottom attached red basic button' v-show="!task.done" @click="completed(task)">
        pending
    </div>
</div>
</template>

<script>
export default {
props: ['task'],
methods: {
    completed(task){
        task.done = true
        this.$emit('complete-todo', task);
    },
       
    Incompleted(task){
       task.done = false
       this.$emit('complete-todo', task);
    }

}
}
</script>

<style>

</style>