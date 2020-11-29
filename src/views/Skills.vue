<template>
  <div class='skills'>
    <h1>Skills</h1>
    <v-simple-table>
      <template v-slot:default>
        <thead>
            <tr>
              <th class="text-left">
                言語
              </th>
              <th class="text-left">
                フレームワーク
              </th>
            </tr>
          </thead>
        <tbody>
          <tr
            v-for="language in languages"
            :key="language.name"
          >
          <td>{{ language.name }}</td>
          <td>{{ language.fw }}</td>         
          </tr>
        </tbody>
  
        <thead>
            <tr>
              <th class="text-left">
                その他
              </th>
              <th class="text-left">
              </th>
            </tr>
          </thead>
        <tbody>
          <tr
            v-for="other in others"
            :key="other.name"
          >
          <td>{{ other.name }}</td>
          <td>{{ other.detail }}</td>         
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
      msg: 'Skills',
      languages: [
        { name: 'Python' ,fw: 'Flask, Django'},
        { name: 'Ruby' ,fw: 'Ruby on Rails' },
        { name: 'JavaScript' ,fw: 'Vue.js' },
      ],
      others:[
        { name: 'Cloud' , detail: 'AWS, GCP'},
        { name: 'tool', detail: 'GitHub, Ansible'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skills{
  margin-top: 50px;
}
h1, h2 {
  font-weight: normal;
}
a {
  color: #42b983;
}
</style>
