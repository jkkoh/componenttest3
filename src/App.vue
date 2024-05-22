<script setup>
import { ref } from 'vue'
import BlogPost from './components/BlogPost.vue'

const posts = ref([
  {id:1 , title:'처음', content:'예시'}
])
const vTitle = ref("")
const vContent = ref("")
const addPost = ()=>{
  posts.value.push({
    id: posts.value.length + 1,
    title: vTitle.value,
    content: vContent.value
  })
  vTitle.value = ''
  vContent.value = ''
}

</script>

<template>
  <div>
    <h4>블로그 글 만들기</h4>
    <p>제목</p>
    <input v-model="vTitle" type="text">
    <br/>
    <p>내용</p>
    <input v-model="vContent" type="text">
    <br/>
    <button @click="addPost">새로운 글 만들기</button>
    <br/>
    <BlogPost 
    v-for="post in posts" 
    :key="post.id" 
    :id="post.id"
    :title="post.title"
    :content="post.content"
    />
  </div>
</template>