<template>
    <div class="container">
        <div class="row">
            <!-- SECTION TITLE -->
            <h1 class="title">Your Instructors</h1>
            <div class="subtitle-container">
                <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.</p>
                <div class="button_1">MORE ABOUT US</div>
            </div>
            <!-- ISTRUCTORS CARDS -->
            <div class="cards-container">
                <div class="row">
                    <!-- CARD -->
                    <div
                    class="card box-shadow"
                    v-for="card in cards"
                    :key="card.id"
                    >
                        <!-- CARD IMG -->
                        <div class="card-img">
                            <img class="img-fluid" :src="`/istructors-img/instructor-${card.image}`" :alt="'foto' + card.name">
                        </div>
                        <!-- CARD DATA -->
                        <h2 class="title">{{card.name}}</h2>
                        <div class="socials">
                            <i class="fab fa-facebook-f"></i>
                            <i class="fab fa-twitter"></i>
                            <i class="fab fa-instagram"></i>
                        </div>
                        <p class="subtitle">{{card.overview}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        cards: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.row{
    flex-direction: column;
    .title{
        padding-bottom: 50px;
        font-size: 40px;
    }
    >.subtitle-container{
        display: flex;
        justify-content: space-between;
        .subtitle{
            max-width: 80%;
            font-size: 20px;
        }  
        .button_1{
            width: 20%;
            height: 40px;
            text-align: center;
        }
    }
    .cards-container{
        >.row{
            flex-direction: row;
            padding: 50px;
            .card{
                width: calc(100% / 3 - 10px);
                margin: 0 10px;
                padding: 30px;
                border-top: 4px solid $green-color;
                border-radius: 10px;
                text-align: center;
                background: #fff;
                .title{
                    padding: 25px 0;
                }
                .socials{
                    color: $tertiary-text-color;
                    i{
                        padding: 0 10px;
                    }
                }
            }
        }
    }
}
</style>