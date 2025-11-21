<template>
  <div class="contact-container">


    <div class="contact-content">
      <form class="left">
        <h1>Contact</h1>
        <div>
          <label for="name">👩‍💻 name: Kwon DongWoon</label>
        </div>
        <div>
          <label for="email">📧 email: kdu9699@gmail.com</label>
        </div>
        <div>
          <label for="message">💻 GitHub: github.com/KwonDongWoon</label>
        </div>
      </form>

      <div class="right">
        <img :src="mimoge" alt="프로필사진" class="profile-mimoge" />
      </div>
    </div>
  </div>
</template>


<script>
import { reactive } from 'vue'
import mimoge from '@/assets/kdw.png'

export default {
  setup() {
    const form = reactive({
      name: "ContactPage",
      email: '',
      message: ''
    })

    return { form, mimoge}
  }
}
</script>

<style>
.contact-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem;
}

.contact-content {
  display: flex;
  align-items: center; /* 높이를 가운데 맞추기 */
  justify-content: space-between;
  gap: 2rem;
}

/* 왼쪽 텍스트 */
.left {
  flex: 1;
  font-size: 1.1rem;
}

/* 오른쪽 이미지 */
.right {
  flex: 1;
  display: flex;
  justify-content: center;
}

.profile-mimoge {
  width: 400px;
  height: auto;
  border-radius: 12px;
}

/* 기본 스타일 유지 */
form div {
  margin-bottom: 1rem;
}
label {
  display: block;
  margin-bottom: 0.3rem;
}

</style>
