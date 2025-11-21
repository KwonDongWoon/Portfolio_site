<template>
  <div class="project-container">
    <h1 class="title">Projects</h1>

    <div class="project-grid">
      <div 
        v-for="project in projects" 
        :key="project.id" 
        class="project-card"
      >
        <a :href="project.github" target="_blank" rel="noopener noreferrer">
          <h2>{{ project.name }}</h2>
          <p>{{ project.description }}</p>
          <span class="more">Github →</span>
        </a>
      </div>
    </div>
  </div>
</template>


<script>
import { ref } from 'vue'

export default {
  name: "ProjectsPage",
  setup() {
    const projects = ref([
      { id: 4, name: 'QR 주문 시스템', description: 'Spring Boot 기반 프로젝트', github:'https://github.com/KwonDongWoon/QR_OrderSite.git'},
      { id: 3, name: '날씨 정보 앱', description: 'Vue + 오픈 API', github:'https://github.com/KwonDongWoon/Weather-app.git'},
      { id: 2, name: '영화검색 사이트', description: 'Vue + 오픈 API + Netlify 배포', github:'https://github.com/KwonDongWoon/Movie_vue.js.git' },
      { id: 1, name: '회의실예약 사이트', description: '전자정부프레임워크(eGovFrame) 기반 프로젝트', github:'https://github.com/KwonDongWoon/eGovFrame_Project01.git' },
    ])
    return { projects }
  }
}
</script>


<style>
.project-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}

.title {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
  font-weight: 700;
}

/* 카드 하나씩 쌓이게 하는 핵심 */
.project-card {
  background: #fff;
  border-radius: 12px;
  padding: 1.5rem;
  border: 1px solid #ddd;
  margin-bottom: 1.5rem;
  transition: 0.25s ease;
  box-shadow: 0px 4px 10px rgba(0,0,0,0.05);
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0px 6px 15px rgba(0,0,0,0.12);
}

.project-card a {
  text-decoration: none;
  color: #333;
  display: block; /* 전체 영역 클릭 가능 */
}

.project-card h2 {
  font-size: 1.4rem;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.desc {
  font-size: 1rem;
  color: #555;
  line-height: 1.5;
  margin-bottom: 1rem;
}

.more {
  font-size: 0.9rem;
  font-weight: 600;
  color: #007bff;
}
</style>
