<template>
    <li class="d-flex justify-content-between align-items-center">
        <span>{{ todoItem.text }}</span>
        <button class="sm red" @click="deleteItem(todoItem)">Sil</button>
      </li>
</template>

<script>
export default {
    props:["todoItem"],
    inject:["deleteItem"],
}
</script>