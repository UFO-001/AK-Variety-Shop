<script setup>
import { data as posts } from "../utils/posts.data.mjs";
console.log(posts, "posts");
</script>

<template>
  <div>{{ posts }}</div>
  <h1>All Blog Posts</h1>
  <ul>
    <li v-for="post of posts">
      <a :href="post.url">{{ post.frontmatter.title }}</a>
      <span>by {{ post.frontmatter.author }}</span>
    </li>
  </ul>
</template>
