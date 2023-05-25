<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from 'vue';

export default {
  name: 'Home',
  components: { PostList },
  setup() {
    const posts = ref([
      { title: 'welcome to the blog', body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus nisl ipsum, sollicitudin nec risus in, fringilla venenatis felis. Aenean laoreet aliquam molestie. Cras ullamcorper velit eu elit fringilla, mollis feugiat quam eleifend. Curabitur quis libero a nibh lobortis semper a a felis. Praesent eget tempor nibh, id auctor orci. Aenean et pretium diam, in facilisis urna. Vivamus venenatis, mi sed rutrum scelerisque, lorem dolor lobortis sapien, sit amet eleifend ligula justo et ante. Praesent egestas justo sed feugiat consequat. Proin ultricies lacus at massa venenatis blandit. Sed efficitur blandit mauris, in dignissim libero faucibus et. Duis quis urna ut sem.', id: 1},
      { title: 'top 5 css tips', body: 'Lorem ipsum', id: 2},
    ])

    return { posts }
  }
}
</script>
