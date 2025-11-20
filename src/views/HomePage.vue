<template>
  <div class="container">
    <div class="left">
      <h1>안녕하세요, 저는 권시루입니다.</h1>
      <div class="image">
        <img :src="image" alt="프로필 이미지" class="profile-img" />
      </div>
    </div>

    <div class="right">
      <h2>About Me</h2>
        저는 성장 중인 개발자로 끊임없이 노력하고 있습니다.<br>
        사용자들에게 가치 있는 서비를 제공하는 개발자가 되기 위해<br>
        계속 공부하고 노력하겠습니다. 감사합니다.<br>
        <br>
        私は成長中の開発者として絶えず努力しています。<br>
        ユーザーに価値のあるサービスを提供する開発者になるために
        ずっと勉強して頑張ります。<br>
        ありがとうございます。
      <h2>Tech Stack</h2>
      <ul>
        <li>Vue 3 + Composition API</li>
        <li>JavaScript / ES6+</li>
        <li>HTML5 / CSS3 / Tailwind</li>
        <li>Git / GitHub</li>
      </ul>
    </div>
  </div>
</template>

<script>
import image from '@/assets/siru.jpg'

export default {
  name: "HomePage",
  setup() {
    return { image }
  }  
}
</script>

<style>
.container {
  display: flex;
  align-items: flex-start; /* 수직 정렬 */
  justify-content: center; /* 중앙 정렬 */
  gap: 50px; /* 왼쪽과 오른쪽 간격 */
  max-width: 1000px; /* 전체 너비 제한 */
  margin: 0 auto; /* 좌우 여백 자동으로 중앙 배치 */
  padding: 20px; /* 여유 공간 */
}

.left, .right {
  flex: 1; /* 공간 균등 분배 */
}

.profile-img {
  width: 300px;
  height: 300px;
  object-fit: cover;
  border-radius: 50%;
}

ul {
  list-style-type: disc;
  padding-left: 20px;
}
</style>