<template>
  <div>
    <h2>My Single Route</h2>
  </div>
</template>

<script>
  import axios from "axios";
  export default {
    name: "Single",
    data: function() {
      return {
        story: {},
        comments: []
      };
    },
    created: function() {
      axios
        .get(
          "https://hacker-news.firebaseio.com/v0/item/" +
            this.$route.params.id +
            ".json"
        )
        .then(res => {
          this.story = res.data;
          this.story.comments = [];
          this.story.kids.forEach(id => {
            axios
              .get("https://hacker-news.firebaseio.com/v0/item/" + id + ".json")
              .then(res => {
                this.$nextTick(() => {
                  (res.data);
                  this.comments.push(res.data);
                });
              })
              .catch(err => {
                (err);
              });
          });
        })
        .catch(err => {
          (err);
        });
    }
  };
</script>
<style scoped></style>
