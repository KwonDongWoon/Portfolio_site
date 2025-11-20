<template>
  <div>
    <h1>Contact</h1>
    <form @submit.prevent="submitForm">
      <div>
        <label for="name">이름:</label>
        <input type="text" id="name" v-model="form.name" required>
      </div>
      <div>
        <label for="email">이메일:</label>
        <input type="email" id="email" v-model="form.email" required>
      </div>
      <div>
        <label for="message">메시지:</label>
        <textarea id="message" v-model="form.message" required></textarea>
      </div>
      <button type="submit">보내기</button>
    </form>
  </div>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup() {
    const form = reactive({
      name: "ContactPage",
      email: '',
      message: ''
    })

    const submitForm = () => {
      alert(`보내기 완료! \n이름: ${form.name}\n이메일: ${form.email}\n메시지: ${form.message}`)
      form.name = ''
      form.email = ''
      form.message = ''
    }

    return { form, submitForm }
  }
}
</script>

<style>
form div {
  margin-bottom: 1rem;
}
label {
  display: block;
  margin-bottom: 0.3rem;
}
input, textarea {
  width: 100%;
  padding: 0.5rem;
  box-sizing: border-box;
}
button {
  padding: 0.5rem 1rem;
  cursor: pointer;
}
</style>
