<template>
  <form class="form" @submit.prevent>
    <h4>Создание поста</h4>
    <my-input
      v-focus
      v-model="post.title"
      type="text"
      placeholder="Название"
    />
    <my-input
      v-model="post.body"
      type="text"
      placeholder="Описание"
    />
    <my-button 
      class="btn btn__create" 
      @click="createPost"
    >
      Создать
    </my-button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post, 'fdfs', 'fdgf fdsf')
      this.post = {
        title: "",
        body: "",
      }
    },
  },
};
</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
}

.btn__create {
  margin-top: 15px;
  align-self: flex-end;
}
</style>
