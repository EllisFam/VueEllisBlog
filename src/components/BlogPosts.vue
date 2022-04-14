<template>
  <div>
    <div class="row">
      <div class="col blog-preview">
        <div v-for="post in BlogPosts" :key="post.id">
          <h2>{{ post.summary }}</h2>
          <p>{{ post.date }}</p>
          <br />
          <p>
            {{ post.post }}
          </p>
          <img :src="'../../public/img' + post.image" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogPosts",
  props: {
    BlogPosts: Array,
  },
  methods: {},
};
</script>

<style scoped>
.blog-preview {
  border: 3px solid rgba(0, 0, 0, 0.664);
  margin: 30px 15%;
}
.blog-preview a {
  color: #6c6955;
  font-weight: bold;
}
.blog-preview a :hover {
  color: #5a6a6e;
  font-weight: bold;
  text-decoration: none;
}

img {
  width: 100px;
}
</style>
