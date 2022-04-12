<template>
  <div>
    <h1>Blog</h1>
    <div class="col quote-of-day">
      <br />
      <p>{{ quote }}</p>
      <p>{{ author }}</p>
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
</style>
