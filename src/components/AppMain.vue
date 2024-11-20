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
<h1 class="text-center">
  Sono la lista dei post
</h1>
<div class="card m-3" v-for="post in posts">
  <div class="card-header">
    {{post.title}}
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item">{{ post.author }}</li>
    <li class="list-group-item">{{post.content}}</li>
  </ul>
</div>
</template>

<style scoped>
</style>