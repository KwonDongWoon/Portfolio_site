<template>
  <div>
    <h1>프로젝트 목록</h1>
    <div v-for="project in projects" :key="project.id" class="project-card">
      <a :href="project.github" target="_blank" rel="noopener noreferrer">
        <h2>{{ project.name }}</h2>
        <p>{{ project.description }}</p>
      </a>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name:"ProjectsPage",
  setup() {
    const projects = ref([
      { id: 4, name: 'QR 주문 시스템', description: 'Spring Boot 기반 학원 프로젝트', github:''},
      { id: 3, name: '날씨 정보 앱', description: 'Vue + 오픈 API', github:'https://github.com/KwonDongWoon/Weather-app.git'},
      { id: 2, name: '영화검색 사이트', description: 'Vue + 오픈 API + Netlify 배포', github:'https://github.com/KwonDongWoon/Movie_vue.js.git' },
      { id: 1, name: '회의실예약 사이트', description: '전자정부프레임워크(eGovFrame) 기반 프로젝트', github:'https://github.com/KwonDongWoon/eGovFrame_Project01.git' },
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
