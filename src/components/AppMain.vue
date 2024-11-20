<script>
import axios from 'axios';

export default {
  data() {
    return {
      apiUrl: "http://127.0.0.1:8000/api/posts",
      posts: [],
    }
  },
  methods: {
    getPosts(){
        axios.get(this.apiUrl)
            .then((response) => {
                // handle success
                this.posts = response.data.results;
                // console.log(this.posts);
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
        }
  },
  created(){
    this.getPosts();
  }
}
</script>

<template>

</template>

<style scoped>
</style>