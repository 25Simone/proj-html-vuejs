<template>
    <div class="container">
        <div class="row">
            <h1>Your Instructors</h1>
            <div class="subtitle-container">
                <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.</p>
                <div class="button_1">MORE ABOUT US</div>
            </div>
            <!-- ISTRUCTORS CARDS -->
            <div class="cards-container">
                <div class="row">
                    <!-- CARD -->
                    <div
                    class="card"
                    v-for="card in cards"
                    :key="card.id"
                    >
                        <!-- CARD IMG -->
                        <div class="card-img">
                            <img class="img-fluid" :src="`/instructor-${card.image}`" :alt="'foto' + card.name">
                        </div>
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
    h1{
        padding-bottom: 50px;
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
                box-shadow: 5px 10px 18px #888888;
                text-align: center;
                .title{
                    color: $secondary-text-color;
                    padding: 25px 0;
                }
                .socials{
                    color: $tertiary-text-color;
                    i{
                        padding: 0 10px;
                    }
                }
                &:hover{
                    transform: scale(1.1);
                }
            }
        }
    }
}
</style>