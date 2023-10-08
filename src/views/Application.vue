<template>
    <div>
        <Header/>
        <Banner/>
        <Featured/>
        <Footer/>
    </div>
</template>

<script>
import Header from '@/components/Application/Header.vue';
import Banner from '@/components/Application/Banner.vue';
import Featured from '@/components/Application/Featured.vue';
import Footer from '@/components/Application/Footer.vue';
export default {
    name: 'Application',
    components: {
        Header,
        Banner,
        Featured,
        Footer
    }
}
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;200;300;400;500;700;900&display=swap');
    @import '@/assets/zayshop/assets/css/bootstrap.min.css';
    @import '@/assets/zayshop/assets/css/templatemo.css';
    @import '@/assets/zayshop/assets/css/custom.css';
    @import '@/assets/zayshop/assets/css/fontawesome.min.css';
</style>