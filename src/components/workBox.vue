<template>
  <div class='workBox'>
    <h1>{{ item.name }}</h1>
    <p>{{ item.description }}</p>
    <img>
    <p>{{ item.url }}</p>
  </div>
</template>

<script>
export default {
  name: 'WorkBox',
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style>
.workBox {
  border-style: solid;
  border-radius: 10px;
  border-width: 1px;
  margin-left: 30px;
  margin-bottom: 30px;
  width: 40%;
}
</style>
