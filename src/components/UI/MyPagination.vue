<template>
  <div class="page__wrapper">
    <div
      v-for="pageNumber in totalPages"
      :key="pageNumber"
      class="page"
      :class="{ 'current-page': page === pageNumber }"
      @click="changePage(pageNumber)"
    >
      {{ pageNumber }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'my-pagination',
  props: {
    totalPages: Number,
    page: Number,
    changePage: Function,
  },
};
</script>

<style scoped>
.page__wrapper {
  margin-top: 15px;
  display: flex;
}

.page {
  border: 1px solid black;
  padding: 10px;
}

.current-page {
  border: 2px solid teal;
}
</style>
