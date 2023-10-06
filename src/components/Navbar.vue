<template>
  <div class="navbar">
    <div @click="$router.push('/')" class="logo">VUE 3</div>
    <div class="navbar__btns">
      <my-button @click="$router.push('/posts')">Посты</my-button>
      <my-button @click="$router.push('/about')">О приложении</my-button>
      <my-button @click="$router.push('/store')">Стор</my-button>
      <my-button @click="$router.push('/composition')">Composition</my-button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.logo {
  cursor: pointer;
}
.navbar {
  padding: 0 15px;
  height: 50px;
  background-color: lightgray;
  box-shadow: 2px 2px 4px gray;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.navbar__btns {
  display: flex;
  gap: 20px;
}
</style>
