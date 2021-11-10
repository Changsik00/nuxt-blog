<template>
  <NuxtLink :to="`/blog/author/${author.name}`">
    <div class="author">
      <img class="author-image" :src="author.image" />
      <div>
        <h6>Author</h6>
        <p>
          {{ author.name }} <br />
          {{ author.bio }}
        </p>
      </div>
    </div>
  </NuxtLink>
</template>
<script>
export default {
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
}
</script>
<style>
.author {
  display: flex;
  padding: 10px;
  border: 1px solid #a0a0a0;
}

.author-image {
  vertical-align: middle;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin: 0 30px;
}
</style>
