<script>
    import AppHeader from '@/components/AppHeader.vue'
    import MobileHeader from '@/components/MobileHeader.vue'

    export default {
        name: "AppVue",
        components: {
            AppHeader,
            MobileHeader
        }
    }
</script>

<template>
    <AppHeader />
    <MobileHeader />
    <RouterView />
</template>

<style lang="scss">
@use './assets/scss/app.scss' as *;

</style>