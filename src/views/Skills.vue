<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <img>
      <table>
        <tbody>
          <ul v-for="(skill,index) in skills" :key="index">
            <li>{{ skill.name }}</li>
          </ul>
        </tbody>
      </table>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      msg: 'Skills',
      skills: [
        { name: 'Python' },
        { name: 'Ruby' },
        { name: 'JavaScript' },
        { name: 'Vue.js' },
        { name: 'AWS' },
        { name: 'GCP' },
        { name: 'GitHub' },
        { name: 'Docker' }
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
