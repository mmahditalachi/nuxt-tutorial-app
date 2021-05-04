<template>
    <div>
        <div class="container">
    <br/>

              <h4>Items</h4>
    <br/>

          <div class="card-deck">
        <TodoItem v-for="item in itemList" :key="item.title" :todoItem ="item"/>
    </div>
    <br/>
    <br/>
    <br/>
        <CreateItem @createItem="createNewItem" />
    </div>
    </div>
</template>

<script>
import TodoItem from '../components/TodoItem'

    export default {
        data(){
            return{
            itemList :[
                {title : "mohi_1", description : "des_1", isDone: false },
                {title : "mohi_2", description : "des_2", isDone: false },
                {title : "mohi_3", description : "des_3", isDone: false },
                {title : "mohi_4", description : "des_4", isDone: false },
            ]     
            }
        },
         components :{
            TodoItem
        },
        methods:{
            createNewItem(todoItem){
                this.itemList.push(todoItem);
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>