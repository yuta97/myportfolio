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
  width: 40%;
}
</style>
