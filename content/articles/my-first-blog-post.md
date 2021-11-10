---
title: My first Blog Post
description: Learning how to use @nuxt/content to create a blog
img: first-blog-post.jpg
alt: my first blog post
slug: my-first-blog-post
updatedAt: 2021.11.10 PM 7:10
author:
  name: Dennis
  bio: All about Dennis
  image: https://avatars.githubusercontent.com/u/6523039?v=4
---

## This is a heading

This is some more info

### This is a sub heading

This is some more info

### This is another sub heading

This is some more info

## This is another heading

This is some more info

# My first blog post 1

## My first blog post 2

### My first blog post 3

#### My first blog post 4

##### My first blog post 5

###### My first blog post 6

Welcome to my first blog post using content module

[adding-a-vue-component](https://nuxtjs.org/tutorials/creating-blog-with-nuxt-content/#adding-a-vue-component)
<author :author="author"></author>
<info-box>
<template #info-box>
This is a vue component inside markdown using slots
</template>
</info-box>

```javascript
export default {
  nuxt: 'is the best',
}
```
