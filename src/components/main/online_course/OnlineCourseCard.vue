<script>


export default {
    name: "Online course card",
    data() {
        return {
            dati: [
                {
                    price: "£40,00", description: "learning to writing as a professional author", numerolezioni: "2", numerostudenti: "50", percorso: "03"
                },
                {
                    price: "free", description: "Costumer-Center Info-Tech Strategies ", numerolezioni: "40", numerostudenti: "20", percorso: "04"
                },
                {
                    price: "£19,00", description: "Open rogrammin course for everyone: Python ", numerolezioni: "17", numerostudenti: "72", percorso: "05"
                },
                {
                    price: "£26,00", description: "Academic Listening and note-taking", numerolezioni: "14", numerostudenti: "67", percorso: "06"
                },
            ]
        }
    },
    methods: {
        getUrl(x) {
            const url = new URL(`../../../assets/img/stock-full-hd-${x}-480x298.jpg`, import.meta.url)
            return url.href
        }
    }


}
</script>

<template>
    <div class="container d-flex ">


        <div class="single-card d-flex   justify-content-between" v-for="i in dati">
            <div class="contenitore-immagine">
                <img :src="getUrl(i.percorso)" alt="immagine">

            </div>
            <div class="text-area">
                <h2>{{ i.price }}</h2>
                <p>{{ i.description }}</p>
                <div>
                    <span><i class="fa-regular fa-file"></i> {{ i.numerolezioni }} lezioni </span>
                    <span class="studenti"><i class="fa-regular fa-user"></i>{{ i.studenti }} studenti</span>

                </div>
            </div>

        </div>


    </div>

</template>

<style lang="scss" scoped>
@use "../../../assets/partials/variale" as *;


.container {
    flex-wrap: wrap;
    justify-content: space-between;
}


.single-card {
    margin: 30px 0;
    align-content: space-between;

    &:hover {
        cursor: pointer;
    }


}

.single-card:hover p {
    color: $color_blue;
}

.contenitore-immagine {
    height: 200px;
    width: 200px;
    border-radius: 50%;
    overflow: hidden;
}

img {
    max-height: 100%;

}



.text-area {
    margin-left: 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

h2 {
    color: $color_blue;
}

p {
    color: $color_dark_blue;
    font-size: 20px;
    margin: 20px 0;
}

span {
    color: $color_dark;
}

.studenti {
    margin-left: 20px;
}
</style>