<script>
import OnlineCourseCard from "./OnlineCourseCard.vue"

export default {
    name: "Online course",
    components: {
        OnlineCourseCard
    }
}
</script>

<template>
    <section>
        <div class="container text-center ">
            <h6>STIMPOLATE TO LEARN?</h6>
            <h3>Featured online courses</h3>
        </div>

        <online-course-card></online-course-card>

        <div class="bottone">

            <button>view all courses <i class="fa-solid fa-arrow-right"></i></button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../../../assets/partials/variale" as *;

section {
    background-color: $color_grey;
}

.container {
    padding-top: 50px;
    margin-top: 50px;
}

h3 {
    color: $color_dark_blue;
}

h6 {
    color: $color_dark;
}

.bottone {
    margin: 50px auto;
    width: 80%;
    text-align: center;

    button {
        color: white;
        background-color: $color_blue;
        padding: 20px 70px;
        border: 2px solid $color_blue;
        border-radius: 20px;
    }
}
</style>