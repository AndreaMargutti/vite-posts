<script>
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
            .then(function (response) {
                // handle success
                console.log(response);
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