<template>
  <div>
    <div class="row">
      <div class="col blog-preview">
        <div v-for="post in blogPosts" :key="post.id">
          <h2>{{ post.summary }}</h2>
          <br />
          <p>
            This is the first blog post on our new website. We are so excited
            about this! Caden has always been better at keeping a journal than
            Courtney has, but we are hoping this website will help us to
            memorialize some of the highlights of our relationship...
            <a href="post.html">(more)</a>
          </p>
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

