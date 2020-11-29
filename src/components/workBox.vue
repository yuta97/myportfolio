<template>
  <div class='workBox'>
    <h1>{{ item.name }}</h1>
    <p>{{ item.description }}</p>
    <img>
    <p> 使用技術：{{ item.skill}} など</p>
    <p v-if="item.url">
      <a :href="item.url" >
        {{ item.urlDescription }}
      </a>
    </p>
    <p v-else>
      {{ item.urlurlDescription }}
    </p>
    <a :href="item.GitHubUrl">
      GitHub
    </a>
    
    
    

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
  padding: 15px 0;
  border-style: solid;
  border-radius: 10px;
  border-width: 1px;
  margin: 30px ;
  width: 42%;
  box-shadow: 5px 5px;
}
</style>
