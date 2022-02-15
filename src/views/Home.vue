<template>
  <div class="home">
    <v-card class="mb-3" outlined v-for="(item, index) in posts" :key="index">
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="text-h5 mb-1">
            {{ item.name }}
          </v-list-item-title>
          <v-list-item-subtitle
            >{{ item.content.substring(0, 50) }}...</v-list-item-subtitle
          >
        </v-list-item-content>

        <v-list-item-avatar tile size="80" color="grey">
          <img :src="require('../res/' + item.id + '.jpg')" alt=""
        /></v-list-item-avatar>
      </v-list-item>

      <v-card-actions>
        <v-btn outlined rounded text @click="open(item)"> Әрі қарай </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
import posts from "../posts.json";

export default {
  name: "Home",
  components: {},
  data: () => ({
    posts: [],
  }),
  created() {
    this.posts = posts;
  },
  methods: {
    open(item) {
      this.$store.state.post = item;
      this.$router.push("/more");
    },
  },
};
</script>
