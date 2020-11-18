<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img>
      <table>
        <tbody>
          <tr v-for="(career,index) in careers" :key="index">
            <th>{{ career.key }}</th>
            <td>{{ career.skill }}</td>
            <td>{{ career.term }}</td>
            <td>{{ career.description }}</td>
          </tr>
        </tbody>
      </table>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      msg: 'career',
      careers: [
        {
          key: 'オーシャンアイズ ',
          skill: 'Python,PHP,GCP・・・etc',
          term: '2020年8月〜現在（週2程）',
          description:
            '漁師さん向けに漁場ナビを提供。サービスの統合やサーバーの構築など'
        },
        {
          key: 'いい生活',
          skill: 'Vue.ls',
          term: '2020年9月　（1週間）',
          description:
            'APIを使い不動産検索アプリ開発'
        },
        {
          key: 'GMO',
          skill: 'Ruby on Rails, Ansible ・・・etc',
          term: '2020年8月　（2週間）',
          description:
            '非機能要件を意識したTodoアプリ開発'
        },
        {
          key: 'フェンリル',
          skill: 'vue.js',
          term: '2020年2月　（1週間）',
          description:
            'ぐるなびAPIを使いVue.jsで検索を表示'
        }
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
a {
  color: #42b983;
}
</style>
