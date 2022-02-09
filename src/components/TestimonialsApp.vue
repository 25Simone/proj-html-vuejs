<template>
    <div class="container-fluid">
        <div class="row">
            <h1 class="title">Testimonials</h1>
            <p class="subtitle">Here's what oue happy drivers had to stay about our services:</p>
            <!-- TESTIMONIALS -->
            <div class="testimonials-data">
                <!-- TESTIMONIAL IMG -->
                <div class="testimonial-img">
                    <img class="img-fluid" :src="`/testimonials-img/testimonial-${testimonials[currentIndex].image}`" :alt="'foto' + testimonials[currentIndex].name">
                </div>
                <!-- OVERVIEW -->
                <p class="subtitle">{{testimonials[currentIndex].overview}}</p>
                <!-- NAME -->
                <h2>{{testimonials[currentIndex].name}}</h2>
                <!-- IMAGES PREVIEW -->
                <div id="circles-container">
                    <div
                    class="circle"
                    :class="{active: i == currentIndex}"
                    v-for="(circle, i) in testimonials"
                    :key="i"
                    @click="GoToTestimonial(i)"
                    >
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        testimonials: Array,
    },
    data(){
        return {
            currentIndex: 0,
        }
    },
    methods: {
        GoToTestimonial(index) {
            this.currentIndex = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.container-fluid{
    background: url('../assets/images/testimonial-background.jpg');
    background-size: cover;
    padding: 250px 0 100px 0;
    .row{
        flex-direction: column;
        align-items: center;
        .title{
            font-size: 45px;
        }
        .subtitle{
            font-size: 20px;
        }
        .testimonials-data{
            display: flex;
            flex-direction: column;
            align-items: center;
            .testimonial-img{
                width: 200px;
                height: 200px;
                border-radius: 50%;
                overflow: hidden;
                margin: 30px 0;
            }
            .subtitle{
                font-size: 20px;
                max-width: 750px;
                text-align: center;
            }
            h2{
                color: $tertiary-text-color;
                padding: 30px 0;
            }
            #circles-container{
                display: flex;
                padding: 20px 0;
                .circle{
                    width: 15px;
                    height: 15px;
                    border: 1px solid $tertiary-text-color;
                    border-radius: 50%;
                    margin: 0 5px;
                }
                .circle.active{
                    background: $tertiary-text-color;
                }
            }
        }
    }
}
</style>