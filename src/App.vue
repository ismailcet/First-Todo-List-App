<template>
  <div class="container">
    <h3 class="text-center">ToDo App</h3>
    <hr class="my-2">
    <AddSection />
    <ListSection />
  </div>
</template>

<script>
import AddSection from "@/components/AddSection.vue";
import ListSection from "@/components/ListSection.vue"
export default{
  components:{
    AddSection,
    ListSection
  },
  data(){
    return{ 
      provideData:{
        todoList:[
        {id:1,text:"Bootcamp #2"},
        {id:2,text:"Bootcamp #2.1"},
        {id:3,text:"Bootcamp #2.2"},
        {id:4,text:"Bootcamp #2.3"},
        {id:5,text:"Bootcamp #2.4"},
        {id:6,text:"Bootcamp #2.5"},
      ]
      }
  }
  },
  provide(){
    return{
      provideData : this.provideData,
      deleteItem:this.deleteItem,
    }
  },
  methods:{
    deleteItem(todoItem){
      this.provideData.todoList = this.provideData.todoList.filter((item)=>item !==todoItem)
    },
    addNewTodo(todo){
      this.provideData.todoList.push({
        id:new Date().getTime(),
        text:todo,
      });
    }
  },
}
</script>