<template>
  <div>
    <h1>Contact</h1>
    <form>
      <div>
        <label for="name">👩‍💻 name: Kwon DongWoon</label>
      </div>
      <div>
        <label for="email">📧 email:kdu9699@gamil.com</label>
      </div>
      <div>
        <label for="message">💻 GitHub:github.com/KwonDongWoon </label>
      </div>
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

    return { form}
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
