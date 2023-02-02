<script>
export default {
    name: "loghi introduction",

    data() {
        return {
            percorsoLoghi: []
        }
    },
    methods: {
        getlogo(x) {
            const url = new URL(`../../../assets/img/client-logo-0${x}.png`, import.meta.url)
            return url.href

        }
    }
}

</script>

<template>

    <div class="container d-flex justify-content-between ">
        <img v-for="i in 6" :src="getlogo(i)" alt="logo" class="logo">

    </div>
</template>

<style scoped lang="scss">
.logo {

    height: 50px;
}
</style>