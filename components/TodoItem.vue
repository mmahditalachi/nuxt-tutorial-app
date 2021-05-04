<template>
  <div>
  <div class="card">
    <div class="card-header">{{todoItem.title}}</div>
    <div class="card-body">{{todoItem.description}}</div> 
    <div class="card-footer">{{todoItem.isDone}}</div>
  </div>
     </div>
</template>

<script>

import "bootstrap/dist/css/bootstrap.min.css";
import "jquery/src/jquery.js";
import "bootstrap/dist/js/bootstrap.min.js";

export default {
  props: {
    todoItem : {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    isDone: {
      type: Boolean
    }
    }
  }
};
</script>

<style lang="scss" scoped></style>
