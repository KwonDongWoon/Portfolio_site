<template>
  <div class="container">
    <div class="left">
      <h1>안녕하세요, 개발자 권동운 입니다.</h1>
      <div class="image">
        <img :src="image" alt="프로필 이미지" class="profile-img" />
        
      </div>

      <div class="about-me">
        <h1>About Me</h1>
          안녕하세요.<br>
          고객에게 좋은 서비스를 개발하고 싶은 권동운 입니다.👩‍💻<br>
          저는 새로운 것을 배우는 걸 좋아하고, 팀원과 함께 아이디어를 나누며 성장하는 걸 중요하게 생각합니다.<br>
          늘 사용자 입장에서 생각하며, 작은 디테일 하나까지 신경 쓰는 개발자가 되겠습니다.💪
    
        </div>

    <div class="skil-tools">
      <h1>Skil & Tools</h1>

      <div class="skil-tools-items">
        <div class="language"><h1>언어</h1></div>
        <div class="front-end"><h1>프론트엔드</h1></div>
        <div class="back-end"><h1>백엔드</h1></div>
      </div>
    </div>

  </div>
    
    <div class="right">
      <div class="growing-developer">
      <h1> 🌱Growing Developer </h1>
        저는 성장 중인 개발자로 끊임없이 노력하고 있습니다.<br>
        사용자들에게 가치 있는 서비를 제공하는 개발자가 되기 위해 계속 공부하고 노력하겠습니다. 감사합니다.<br>
        <br>
        私は成長中の開発者として絶えず努力しています。<br>
        ユーザーに価値のあるサービスを提供する開発者になるために
        ずっと勉強して頑張ります。<br>
        ありがとうございます。
      </div>
      <div>
        <img :src="coding" alt="코딩이미지" class="coding" />
      </div>
    </div>
  </div>
</template>

<script>
import image from '@/assets/siru.jpg'
import coding from '@/assets/codingimg.png'

export default {
  name: "HomePage",
  setup() {
    return { image, coding }
  }  
}
</script>

<style>
.title {
  text-align: center;
}

.container {
  display: flex;
  align-items: flex-start; /* 수직 정렬 */
  justify-content: center; /* 중앙 정렬 */
  gap: 50px; /* 왼쪽과 오른쪽 간격 */
  max-width: 1000px; /* 전체 너비 제한 */
  margin: 0 auto; /* 좌우 여백 자동으로 중앙 배치 */
  padding: 10px; /* 여유 공간 */
  padding-left: 60px;
  padding-right: 60px;
}

.left, .right {
  flex: 1; /* 공간 균등 분배 */
}

.right {
  display: flex;
  flex-direction: column; /* 세로로 쌓기 */
  justify-content: flex-start;
  align-items: center;
  gap: 40px; /* 내용과 이미지 간 간격 */
}

.profile-img {
  width: 300px;
  height: 300px;
  object-fit: cover;
  border-radius: 50%;
}

.coding{
  padding-top: 30px;
  width: 400px;
  height: 380px;
}

ul {
  list-style-type: disc;
  padding-left: 20px;
}

.skil-tools {
  margin-top: 60px;
  padding-top: 150px;
}

.about-me{
  padding-top: 120px;
}

.growing-developer {
  padding: 50px;
}

.skil-tools {
  width: 100%;
}

.skil-tools h1:first-child {
  margin-bottom: 20px;
}

.skil-tools-items {
  display: flex;
  gap: 20px;
}

.skil-tools-items > div {
  flex: 1;
  text-align: center;
}
</style>