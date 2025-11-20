<template>
  <div>
    <h1>프로젝트 목록</h1>
    <div v-for="project in projects" :key="project.id" class="project-card">
      <h2>{{ project.name }}</h2>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name:"ProjectsPage",
  setup() {
    const projects = ref([
      { id: 1, name: '영화검색 사이트', description: 'Vue + Netlify 배포' },
      { id: 2, name: 'QR 주문 시스템', description: 'Spring Boot 기반 학원 프로젝트' },
    ])
    return { projects }
  }
}
</script>

<style>
.project-card {
  border: 1px solid #ccc;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 6px;
}
</style>
