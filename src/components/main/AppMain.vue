<script>

import AppLoghi from "./introduction/AppLoghi.vue"
import SpliceScreen from "./SpliceScreen.vue"

export default {
    name: "AppMain",
    components: {

        AppLoghi, SpliceScreen
    }
}
</script>

<template>
    <splice-screen orientamento="sx"></splice-screen>
    <app-loghi></app-loghi>

</template>