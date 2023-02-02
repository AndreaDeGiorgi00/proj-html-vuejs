<script>
export default {
    name: "smart tutoring card",
    data() {
        return {
            dati: [
                { posizione: "01", title: "Customize preference", description: "Learners are given right toarrange and customize their study schedule and timetable based on prefereces", goto: "start here" },
                { posizione: "02", title: "Cloud Storage", description: "You can store online lessons via online cloud or download to your device and revise lessins on the way", goto: "Get Free Quote" },
                { posizione: "03", title: "Multimedia Channels", description: "We provide study materials with varius formats vide, audio, slides, doc, prints, books and applications", goto: "start now" },

            ]
        }
    },
    methods: {
        getUrl(x) {
            const url = new URL(`../../../assets/img/home-2-image-box-${x}.png`, import.meta.url)
            return url.href
        }
    }
}
</script>

<template>
    <div class="contenitore " v-for="i in dati">
        <img :src="getUrl(i.posizione)" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{ i.title }}</h5>
            <p class="card-text">{{ i.description }}</p>
            <a href="#">{{ i.goto }} <i class="fa-solid fa-arrow-right"></i></a>
        </div>
    </div>

</template>


<style lang="scss" scoped>
@use "../../../assets/partials/variale" as *;

.contenitore {
    width: calc(100%/3 - 100px);

    img {
        max-width: 80%;
        margin: 30px 0;
    }

    a {
        text-decoration: none;
    }
}
</style>