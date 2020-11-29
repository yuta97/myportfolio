<template>
  <div class='about'>
    <h1>Works</h1>
    <v-simple-table>
      <template v-slot:default>
        <tbody>
          <tr
            v-for="item in infos"
            :key="item.key"
          >
            <td>{{ item.key }}</td>
            <td v-if="item.url">
                <a :href="item.url" >
                  {{ item.value }}
                </a>
              </td>
              <td v-else>
                {{ item.value }}
              </td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
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
      ],
      desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
          },
          {
            name: 'Eclair',
            calories: 262,
          },
          {
            name: 'Cupcake',
            calories: 305,
          },
          {
            name: 'Gingerbread',
            calories: 356,
          }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about{
  margin-top: 50px;
}
h1, h2 {
  font-weight: normal;
}
a {
  color: #42b983;
}
</style>
