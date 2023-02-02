<script >
import AppMain from "./components/main/AppMain.vue"
import AppHeader from "./components/header/AppHeader.vue"
import AppFooter from "./components/footer/AppFooter.vue"


export default {
    components: {
        AppMain,
        AppHeader,
        AppFooter,
    }
}
</script>

<template>
    <app-header></app-header>
    <app-main></app-main>
    <app-footer></app-footer>

</template>

<style lang="scss">

</style>
