<script>
export default {
    name: "splice screen",
    props: ["orientamento"],
    methods: {
        direzione(x) {
            return true
        }
    },
    computed: {
        calcDirection() {
            if (this.orientamento == "sx") {

                return true
            } else {
                return false
            }
        }
    }

}
</script>

<template>
    <div v-if="calcDirection" class="first">
        <div class="container d-flex align-items-center justify-content-around ">
            <div class="text-area">
                <h1>Distant learning for further expasion</h1>
                <p>Learning is a life-long journey that in fact we never find the terminate stop. Stop searching,
                    enjoy the process.</p>
                <button><i class="fa-solid fa-download"></i> download free guide</button>
                <p>have questions? <a href="#">get Free sample</a></p>
            </div>

            <div>
                <img src="../../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg"
                    alt="profilo">
            </div>
        </div>
    </div>
    <div v-else class="second">
        <div class="container d-flex justify-content-between">
            <div class="video">
                <img src="../../assets/img/icon-youtube-play.png" alt="yb" class="yb">
                <img src="../../assets/img/home-2-popup-video-poster.jpg" alt="yb">

            </div>
            <div class="text-area ">
                <p>GET STARTED EFFORTLY</p>
                <h1>enjoy our <span>companionship</span></h1>
                <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some
                    hidden hints of early-bird rewards as well</p>
                <a href="#"> download free guidebook <i class="fa-solid fa-arrow-right"></i></a>
            </div>
        </div>
    </div>
</template>



<style lang="scss" scoped>
@use "../../assets/partials/variale" as *;

.first {
    margin-bottom: 50px;

    .text-area {
        width: 40%;

        p {
            margin: 20px 0;
            color: $color_dark;
        }
    }

    img {
        border-radius: 50%;
        height: 500px;
    }

    h1 {
        color: $color_dark_blue;
    }

    button {
        background-color: $color_blue;
        padding: 15px 50px;
        border: 1px solid $color_blue;
        color: white;
        border-radius: 20px;
    }
}


.second {
    .container {
        margin-bottom: 50px;
    }

    .video {
        position: relative;
    }

    .yb {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-25%, -25%);
    }

    .text-area {
        width: 30%;
        display: flex;
        flex-direction: column;
        justify-content: center;

        span {
            color: $color_blue;
        }

        a {
            color: $color_blue;

        }
    }
}
</style>