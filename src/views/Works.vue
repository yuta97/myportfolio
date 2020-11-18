<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="works">
      <work-box v-for="work in works" :key="work.name"  :item="work"/>
    </div>
  </div>
</template>

<script>
import workBox from '@/components/workBox'

export default {
  name: 'about',
  components: {
    workBox
  },
  data () {
    return {
      msg: 'Works',
      works: [
        {name: 'J検索くん', url: '', image: '', description: 'サッカーJリーグのデータをスクレイピングして、検索できるサービス', skill: 'Python'},
        {name: '課題通知くん', url: '', image: '', description: '大学の課題サイトをスクレイピングし、未修の課題をLineに通知してくれる', skill: 'Python'},
        {name: 'ポートフォリオ', url: '', image: '', description: 'このサイトです', skill: 'Vue.js'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.works {
  display: flex;
  flex-wrap: wrap;
}
</style>
