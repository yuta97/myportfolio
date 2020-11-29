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
        {name: 'J検索くん', url: 'http://j-search.s3-website-ap-northeast-1.amazonaws.com/', urlDescription: '検索サイトに飛べます', image: '', description: 'サッカーJリーグのデータをスクレイピングして、検索できるサービス', skill: 'Python', GitHubUrl: 'https://github.com/yuta97/j-search'},
        {name: '課題通知くん', url: 'https://qiita.com/yokubarisanyuyu/items/2ef369dc02cf78747b29', urlDescription: 'Qitaでの解説記事',image: '', description: '大学の課題サイトをスクレイピングし、未修の課題をLineに通知してくれるツール', skill: 'Python', GitHubUrl: 'https://github.com/yuta97/untask_notify_by_lambda'},
        {name: 'ポートフォリオ', url: '', urlDescription: '',image: '', description: 'このサイトです', skill: 'Vue.js', GitHubUrl: 'https://github.com/yuta97/myportfolio'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  padding: 50px 0;
  /* background-color: #CCFFCC; */
}
h1, h2 {
  top: 50%;
  /* 中央におきたい */
  font-weight: normal;
  margin-bottom: 50px;
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
  margin: 0 10%;
}
</style>
