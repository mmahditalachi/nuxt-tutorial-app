<template>
    <div class="container">
  <h4>create new item</h4>
  <form @submit="$emit('createItem', todoItem)">
    <div class="form-group">
      <label for="title">title:</label>
      <input type="title" class="form-control" id="title" placeholder="Enter title" name="title" v-model="todoItem.title">
    </div>
    <div class="form-group">
      <label for="description">description:</label>
      <input type="description" class="form-control" id="description" placeholder="Enter description"
       name="description" v-model="todoItem.description">
    </div>
    <div class="form-group form-check">
      <label class="form-check-label">
        <input class="form-check-input" type="checkbox" name="remember" v-model="todoItem.isDone"> done
      </label>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
</div>
</template>

<script>
    export default {
        data(){
            return{
                todoItem : {
                    title : "",
                    description : "",
                    isDone : false,
                },
            }
        },
        emits: {
              createItem : (todoItem) =>{
                  return todoItem;
              }
        }            
    }
</script>

<style lang="scss" scoped>

</style>