<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img>
      <table>
        <tbody>
          <tr v-for="(info,index) in infos" :key="index">
            <th>{{ info.key }}</th>
            <td v-if="info.url">
              <a :href="info.url" >
                {{ info.value }}
              </a>
            </td>
            <td v-else>
              {{ info.value }}
            </td>
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
      msg: 'About',
      infos: [
        {key: 'Name', value: '増井悠太', url: ''},
        {key: 'University', value: '京都大学　工学部　地球工学科', url: ''},
        {key: 'GitHub', value: 'yuta97', url: 'https://github.com/yuta97'},
        {key: 'Qiita', value: 'yokubarisanyuyu', url: 'https://qiita.com/yokubarisanyuyu'},
        {key: 'Twitter', value: 'yokubarisanyuyu', url: 'https://twitter.com/yokubarisanyuyu'}
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
</style>
