/<template>
  <div class="about">
    <Top/>
    <Middle/>
    <Bottom/>
  </div>
</template>
<script>
  import Top from '@/components/AboutPage/Top.vue';
  import Middle from '@/components/AboutPage/Mid.vue';
  import Bottom from '@/components/AboutPage/Bottom.vue';
  export default{
    components:{
      Top,
      Middle,
      Bottom
    },
    mounted() {
    const jqueryScript = document.createElement('script');
    jqueryScript.src = 'https://code.jquery.com/jquery-3.6.0.min.js';
    jqueryScript.onload = () => {
      const externalScript = document.createElement('script');
      externalScript.src = 'admin/dist/js/app.js';
      document.body.appendChild(externalScript);
    };
    document.body.appendChild(jqueryScript);
  }
  }
</script>