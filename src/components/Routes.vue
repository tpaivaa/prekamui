<template>
  <div class="hello">
    <div class='' v-for="route in routes" :key="route.id">
      <p>{{route.routeId}}</p>
      <p>{{route.route.prefix}}</p>
      <p>{{route.route.dest}}</p>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
export default {
  name: 'Routes',
  data () {
    return {
      routes: [
        {
          operatorId: 1,
          routeId: 1,
          route: {
            prefix: '991',
            dest: '10.10.10.1'
          }
        },
        {
          operatorId: 1,
          routeId: 2,
          route: {
            prefix: '992',
            dest: '10.10.10.1'
          }
        }
      ]
    }
  },
  mounted () {
    let self = this
    axios.get('https://routes')
      .then((response) => { self.routes = response.data; console.log('Data: ', response.data) })
      .catch((error) => { console.log('Error: ', error) })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
