<template>
  <div>
    BookList
    <ul>
      <li @click="showBookDetail(book.id)" v-for="book in books" :key="book.id">
        {{ book.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "BookList",
  data() {
    return {
      bookIndex: -1,
      books: [
        { id: 1, title: "title1", content: "naiyou1" },
        { id: 2, title: "title2", content: "naiyou2" },
        { id: 3, title: "title3", content: "naiyou3" },
      ],
    };
  },
  methods: {
    showBookDetail(id) {
      this.bookIndex = id - 1;
      console.log(this.bookIndex);
      this.$router.push({
        name: 'BookDetail',
        params: {
          id: this.books[this.bookIndex].id,
          title: this.books[this.bookIndex].title,
          content: this.books[this.bookIndex].content,
        }
      })

    }
  }
};
</script>

<style></style>
