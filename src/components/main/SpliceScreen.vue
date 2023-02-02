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
        <div class="container d-flex align-items-center justify-content-around">
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
    }
}
</style>