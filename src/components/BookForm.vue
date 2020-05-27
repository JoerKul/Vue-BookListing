<template>
  <div>
    <form class="" action="#" method="post">
      <input
        type="text"
        name="title"
        value=""
        v-model="bookTitle"
        placeholder="Book Title"
      />
      <input
        type="text"
        name="author"
        value=""
        v-model="bookAuthor"
        placeholder="Book Author"
      />
      <button
        type="submit"
        name="button"
        v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)"
      >
        Add Book
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: "BookForm",
  props: ["books"],
  data() {
    return {
      bookTitle: "",
      bookAuthor: "",
    };
  },
  methods: {
    bookSubmit: function (bookTitle, bookAuthor) {
      console.log("book submited");
      this.$emit("addBook", bookTitle, author);
    },
  },
};
</script>

<style scoped></style>
