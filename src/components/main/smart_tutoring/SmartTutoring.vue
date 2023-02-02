<script>
import SmartTutoringCard from "./SmartTutoringCard.vue"
export default {
    name: "smart tutoring",
    components: {
        SmartTutoringCard
    }
}
</script>

<template>
    <div class="text-center">
        <h6>MAXCOACH AVIABLE NOW!</h6>

        <h2>access <span>smart tutoring </span> program for benefits</h2>
    </div>
    <div class="container d-flex justify-content-between">
        <smart-tutoring-card></smart-tutoring-card>

    </div>

</template>


<style lang="scss" scoped>
@use "../../../assets/partials/variale" as *;

span {
    color: $color_blue;
}

.container {
    margin-top: 50px;
    margin-bottom: 100px;
}
</style>