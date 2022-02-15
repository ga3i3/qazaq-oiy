<template>
  <div class="more">
    <img :src="require('../res/' + $store.state.post.id + '.jpg')" alt="" />
    <h1 class="mt-10 mb-2">{{ $store.state.post.name }}</h1>
    <p>{{ $store.state.post.content }}</p>
  </div>
</template>

<script>
export default {
  name: "More",
  created() {
    if (this.$store.state.post == "") {
      this.$router.push("/");
    }
  },
};
</script>

<style lang="scss" scoped>
img {
  width: 100%;
  height: 300px;
  object-fit: contain;
  background-color: #f1f1f1;
  border-radius: 15px;
}
</style>