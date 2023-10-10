<template>
    <div>
        <Hero/>
        <Why/>
        <Product/>
        <Client/>
        <Footer/>
    </div>
</template>
<script>
import Hero from '@/ApplicationComponents/Hero.vue';
import Why from '@/ApplicationComponents/Why.vue';
import Product from '@/ApplicationComponents/Product.vue';
import Client from '@/ApplicationComponents/Client.vue';
import Footer from '@/ApplicationComponents/Footer.vue';
export default {
    name: 'Application',
    components: {
        Hero,
        Why,
        Product,
        Client,
        Footer
    },
    mounted() {
        const scriptPaths = [
        '/famms/js/jquery-3.4.1.min.js',
        '/famms/js/owlcarousel.js',
        '/famms/js/popper.min.js',
        '/famms/js/bootstrap.js',
        '/famms/js/custom.js',
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
        } catch (error) {
            console.error('Failed to load scripts:', error);
        }
        };
        loadScripts();
    }
}
</script>
<style scoped>
   @import '@/assets/famms/css/bootstrap.css';
   @import '@/assets/famms/css/style.css';
   @import '@/assets/famms/css/responsive.css';
</style>