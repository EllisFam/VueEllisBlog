<template>
  <div>
    <h1>Blog</h1>
    <div class="col quote-of-day">
      <br />
      <p>{{ quote }}</p>
      <p>{{ author }}</p>
    </div>
    <div class="row">
      <div class="col blog-preview">
        <h2>First Blog Post</h2>
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
</template>

<script>
export default {
  name: "BlogView",
  data() {
    return {
      quote: "",
      author: "",
    };
  },

  created() {
    this.getQuote();
  },

  methods: {
    getQuote() {
      let url = "https://cors-anywhere.herokuapp.com";
      url += "/inspiration.goprogram.ai";
      fetch(url)
        .then((response) => {
          return response.json();
        })
        .then((json) => {
          console.log("json: " + json);
          this.quote = '"' + json.quote + '"';
          this.author = "-" + json.author;
        })
        .catch((error) => {
          console.log("error" + error);
          const quote =
            "When you exceed the 'quote of the day' API call limits, gotta have a backup quote.";
          const author = "The Ellis'";
          this.quote = '"' + quote + '"';
          this.author = "-" + author;
        });
    },
  },
};
</script>

<style scoped>
.quote-of-day {
  font-style: italic;
  text-align: center;
}
/* Blog */
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
.blog-post {
  border: 3px solid rgba(0, 0, 0, 0.664);
  margin: 30px 15%;
  padding: 7px 10px;
}
.blog-post h4 {
  font-size: 15px;
}
.flex-wrapper {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  justify-content: space-between;
}
#author {
  padding-left: 25px;
}
</style>
