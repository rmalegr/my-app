
<template>
  <MainLayout>
    <div class="mx-auto max-w-[500px] overflow-hidden">
      <div class="mx-auto max-w-[500px] overflow-hidden">
        <div id="Posts" class="px-4 max-w-[600px] mx-auto">
          <div v-if="isPosts" v-for="post in posts" :key="post">
            <Post :post="post" @isDeleted="posts = []" />

          </div>
        </div>
      </div>
    </div>
  </MainLayout>
</template>

<script setup>
import MainLayout from '../layouts/MainLayout.vue';
import Post from '../components/Post.vue'
import { useUserStore } from '../stores/user';
const userStore = useUserStore()
let posts = ref([])
let isPosts = ref(true)
let isLoading = ref(false)

onBeforeMount(() => {
  posts.value = [
    {
      name: 'Rodrigo',
      image: 'https://placehold.co/100',
      text: 'this is the title',
      picture: 'https://placehold.co/500'
    }
  ]
})
</script>