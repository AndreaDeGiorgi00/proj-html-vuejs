<script>

import AppLoghi from "./introduction/AppLoghi.vue"
import SpliceScreen from "./SpliceScreen.vue"
import OnlineCourse from "./online_course/OnlineCourse.vue"

export default {
    name: "AppMain",
    components: {

        AppLoghi, SpliceScreen, OnlineCourse,
    }
}
</script>

<template>
    <splice-screen orientamento="sx"></splice-screen>
    <app-loghi></app-loghi>
    <online-course></online-course>

</template>