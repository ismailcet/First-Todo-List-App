<template>
    <div>
        <TodoList/>
        <ResultBar/>
    </div>
</template>

<script>
import TodoList from "@/components/TodoList.vue";
import ResultBar from "@/components/ResultBar.vue";
export default {
    components:{
        TodoList,
        ResultBar
    },
}
</script>