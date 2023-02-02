<script>
import AppLinksAndSerchBar from "./AppLinksAndSerchBar.vue"
export default {
    name: "App Header",
    components: {
        AppLinksAndSerchBar
    }
}
</script>
<template>

    <div class="container d-flex justify-content-between align-items-center">
        <img src="../../assets/img/dark-logo.png" alt="">
        <app-links-and-serch-bar></app-links-and-serch-bar>
    </div>

</template>

<style lang="scss" scoped>
.container {

    height: 70px;

    img {
        max-width: 170px;
    }
}
</style>