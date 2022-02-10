<template>
<div>
    <div class="container-fluid">
        <div class="container">
            <div class="row">
                <!-- COURSES INFORMATION -->
                <div id="courses-information">
                    <img src="@/assets/images/new-corner.jpg" alt="new corner image">
                    <h1>Courses</h1>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.</p>
                    <div class="button_1">COURSE INFORMATION</div>
                </div>
                <!-- COURSES CARDS -->
                <div class="cards-container row">
                    <div
                    class="course-card"
                    v-for="card in cards"
                    :key="card.id"
                    >
                        <div class="card-img">
                            <img class="img-fluid" :src="`/courses-img/${card.image}`" :alt="card.name + 'thumb'">
                        </div>
                        <h2 class="course-title">{{card.name}}</h2>
                        <div class="button_2">LEARN MORE</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <img class="template-svg" src="@/assets/svg/driving-triangle.svg" alt="">
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

.container-fluid{
    background: url('../assets/images/promise-background.jpg') bottom;
    background-size: cover;
    padding-bottom: 50px;
    .row{
        align-items: center;
    }
    #courses-information{
        background: #fff;
        margin-right: 20px;
        padding: 60px 40px;
        width: 35%;
        border-radius: 10px;
        box-shadow: 5px 10px 18px #888888;
        position: relative;
        top: -30px;
        overflow: hidden;
        text-align: center;
        img{
            position: absolute;
            top: 0;
            left: 0;
            width: 80px;
        }
        h1{
            font-size: 36px;
            color: $secondary-text-color;
        }
        p{
            line-height: 30px;
            color: $tertiary-text-color;
            padding: 50px 0;
        }
        .button_1{
            display: inline-block;
        }
    }
    .cards-container{
        width: 65%;
        .course-card{
            width: calc(100% / 3);
            padding: 0 20px;
            text-align: center;
            .course-title{
                color: $blue-color;
                font-size: 20px;
                padding: 20px 0;
            }
            .button_2{
                font-size: 12px;
            }
        }
    }
}
.template-svg{
    transform: rotate(360deg);
    width: 100%;
    height: 150px;
    margin-top: -2px;
}
</style>