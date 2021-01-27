<template>
  <div>
    <slot-test>
      <div v-for="post in posts" :key="post">
        <h3>{{ post.title }}</h3>
        <p>{{ post.content }}</p>
      </div>
    </slot-test>
    <button @click="getir">İçerikleri Getir</button>
    <button @click="posts = []">İçerikleri Sil</button>
  </div>
</template>

<script>
import SlotTest from "./components/SlotTest.vue";

export default {
  components: {
    SlotTest,
  },
  data() {
    return {
      posts: [],
    };
  },
  methods: {
    getir() {
      this.posts = [
        {
          id: 1,
          title: "Lorem Title 12321321",
          content: "Lorem Content 67534234",
        },
        {
          id: 2,
          title: "Lorem Title 456345345",
          content: "Lorem Content 34567433",
        },
        {
          id: 3,
          title: "Lorem Title 1233554",
          content: "Lorem Content 457642",
        },
      ];
    },
  },
};
</script>
