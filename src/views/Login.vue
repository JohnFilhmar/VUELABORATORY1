<template>
  <div>
    <Form/>
  </div>
</template>

<script>
import Form from '@/LoginComponents/login_form.vue';
export default {
  name: 'Login',
  components : {
    Form
  },
  mounted() {
    const scriptPaths = [
      'admin/assets/libs/jquery/dist/jquery.min.js',
      'admin/assets/libs/popper.js/dist/umd/popper.min.js',
      'admin/assets/libs/bootstrap/dist/js/bootstrap.min.js'
    ];

    const loadScript = (path) => {
      return new Promise((resolve, reject) => {
        const script = document.createElement('script');
        script.src = path;
        script.onload = resolve;
        script.onerror = reject;
        document.body.appendChild(script);
      });
    };

    const loadScripts = async () => {
      try {
        await loadScript(scriptPaths[0]); // Load jQuery first
        for (let i = 1; i < scriptPaths.length; i++) {
          await loadScript(scriptPaths[i]);
        }
        $('[data-toggle="tooltip"]').tooltip();
        $(".preloader").fadeOut();
      } catch (error) {
        console.error('Failed to load scripts:', error);
      }
    };

    loadScripts();
  }
}
</script>
<style scoped>
@import '@/assets/admin/dist/css/style.min.css';
</style>