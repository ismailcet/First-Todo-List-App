<template>
    <div>
        <label for="todoText"></label>
        <input @keydown.enter="addNewTodo($event.target.value)" type="text" id="todoText" placeholder="Bir Şeyler yazınız">
    </div>
</template>

<script>
export default {
    props:{
        addNewTodo:{
            type:Function,
            required:true
        }
    },
    methods:{
    }
}
</script>