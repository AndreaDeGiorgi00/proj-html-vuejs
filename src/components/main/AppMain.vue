<script>

import AppLoghi from "./introduction/AppLoghi.vue"
import SpliceScreen from "./SpliceScreen.vue"
import OnlineCourse from "./online_course/OnlineCourse.vue"
import SmartTutoring from "./smart_tutoring/SmartTutoring.vue"

export default {
    name: "AppMain",
    components: {

        AppLoghi, SpliceScreen, OnlineCourse, SmartTutoring
    }
}
</script>

<template>
    <splice-screen orientamento="sx"></splice-screen>
    <app-loghi></app-loghi>
    <online-course></online-course>
    <smart-tutoring></smart-tutoring>
    <splice-screen orientamento="dx"></splice-screen>
</template>