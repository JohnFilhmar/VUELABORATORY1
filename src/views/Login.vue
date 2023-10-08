<template>
  <div class="main-wrapper">
    <Form/>
  </div>
</template>

<script>
import Form from '@/components/Login/login_form.vue';
export default {
  name: 'Login',
  components : {
    Form
  }
}
</script>

<style scoped>
@import '@/assets/admin/assets/css/style.min.css';
</style>