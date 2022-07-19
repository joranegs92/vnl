<template>
  <div class="hello">
    <head>
      <title>Hello</title>
      <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
    </head>
    <body>
    <button @click="save()" >안녕하세요 </button>
    </body>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'HomeView',
  data () {
    return {

    }
  },
  methods : {
    save : function() {
      axios.post('/api/test/post')
          .then(() => {
            console.log("test")
          })
    }
  }
}
</script>
