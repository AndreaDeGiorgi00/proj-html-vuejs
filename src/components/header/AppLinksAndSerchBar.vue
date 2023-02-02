<script>
import { store } from "../../data/store"
export default {
    name: "links",
    data() {
        return {
            store,
            counter: 0,
            titles: ["", "home", "pages", "courses", "features", "blogs"]
        }
    },
    methods: {
        makesActive(x) {
            if (this.counter == x) {

                this.counter = 0
            } else {

                this.counter = x
            }



        },
        isActive(x) {
            if (x == this.counter) {
                return "active"
            } else {
                return "not-active"
            }
        }
    },


}
</script>
<template>

    <div class="contenitore d-flex align-items-center justify-content-end">
        <div class="links">
            <ul class="d-flex  justify-content-between">
                <li v-for="i in 5">
                    <div class="contenitore-menù">

                        <div class="titolo d-flex justify-content-between align-items-center" @click="makesActive(i)">
                            <span>{{ this.titles[i] }} </span><i class="fa-solid fa-angle-down"></i>

                        </div>

                        <div class="menù-a-tendina" :class="isActive(i)">
                            <ul>

                                <li>Start Here</li>
                                <li>Success Story</li>
                                <li>About me</li>
                                <li>About us 01</li>
                                <li>About us 02</li>
                                <li>About us 03</li>
                                <li>Contact me</li>
                                <li>Contact us</li>
                                <li>Purchase Guide</li>
                                <li>Privacy Policy</li>
                                <li>Terms of Service</li>


                            </ul>
                        </div>

                    </div>

                </li>

            </ul>
        </div>
        <i class="fa-regular fa-circle-user"></i>
        <input type="text" placeholder="search...." v-model="store.inputRicerca">
    </div>

</template>

<style scoped lang="scss">
.contenitore {
    width: 70%;
    height: 100%;

    i:hover {
        color: #20AD96;
    }

    .links {
        width: 70%;
        margin-right: 2rem;
    }

    ul {
        margin: 0;
        height: 100%;
        padding: 0;
    }

    li {
        list-style-type: none;
        width: 100%;
    }

    input {
        margin-left: 10px;
    }

    .titolo {
        width: 30%;
        cursor: pointer;

        &:hover {
            color: #20AD96;
        }

    }



    .contenitore-menù {
        position: relative;
    }

    .menù-a-tendina {

        position: absolute;
        top: 120%;
        left: 0;
        display: none;

        &.active {
            display: block;
        }

        ul {
            border-bottom: 3px solid #20AD96;
        }

        li {
            padding: 5px;
            color: rgb(59, 59, 59);
            cursor: pointer;

            &:hover {
                color: #20AD96;

            }
        }


    }
}
</style>