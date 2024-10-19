<template>
    <div>
        <Header />
        <nuxt :key="$route.fullPath" />
        <Footer />
        <Sidebar />
    </div>
</template>

<script>
import Header from "@/components/header/header";
import Footer from "@/components/footer/footer";
import Sidebar from "@/components/sidebar/sidebar.vue";



export default {
    name: "Default",
    components: {
        Header,
        Footer,
        Sidebar
    }
};
</script>

<style lang="scss">
.page-main {
    position: relative;
    z-index: $zMain;
}
</style>