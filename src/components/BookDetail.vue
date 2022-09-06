<template>
  <div>
    BookDetail
    <p>id: {{ id }}</p>
    <p>title: {{ title }}</p>
    <p>content: {{ content }}</p>
    {{ books[bookIndex].title }}
  </div>
</template>

<script>
export default {
  props: {
    id: Number,
    title: String,
    content: String
  },
  data() {
    return {
      bookIndex: this.$route.params.id - 1,
      books: [
        { id: 1, title: "title1", content: "naiyou1" },
        { id: 2, title: "title2", content: "naiyou2" },
        { id: 3, title: "title3", content: "naiyou3" },
      ],
    };
  },
  created() {
    if(this.$route.params.id > this.books.length ) {
      this.$router.push('/book')
    }
  }
}
</script>

<style>

</style>