<template>
    <div>
        <!-- LATEST NEWS -->
        <div class="container">
            <div class="row">
                <h1 class="title">Latest News</h1>
                <div class="posts">
                    <div>
                        <img class="img-fluid" src="@/assets/images/blog-choosecar-700x441.jpg" alt="post image">
                        <h2 class="post-title">What Car to Start With?</h2>
                        <div class="post-date">February 7th, 2019 | <span>0 Comments</span> </div>
                        <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing.</p>
                    </div>
                    <div>
                        <img class="img-fluid" src="@/assets/images/blogpost-10and2-700x441.jpg" alt="post image">
                        <h2 class="post-title">Avada Driving School Expanding</h2>
                        <div class="post-date">February 7th, 2019 | <span>0 Comments</span> </div>
                        <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing.</p>
                    </div>
                </div>
                <div class="button_1">MORE FROM THE BLOG</div>
            </div>
        </div>
        <!-- TRIANGLE  SVG -->
        <span class="svg-container">
            <svg class="template-svg" xmlns="http://www.w3.org/2000/svg" version="1.1" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#fff;padding:0;"><path d="M-1 -1 L50 99 L101 -1 Z"></path></svg>
        </span>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.container{
    border-top: 4px solid $blue-color;
    border-radius: 10px 10px 0 0;
    background: #fff;
    padding: 40px;
    box-shadow: 5px 10px 18px $blue-color;
    .row{
        flex-direction: column;
        align-items: center;
        .title{
            padding: 30px 0;
            font-size: 40px;
        }
        .posts{
            display: flex;
            width: 100%;
            >div{
                width: 50%;
                padding: 0 15px;
                text-align: center;
                h2{
                    color: $green-color;
                    padding: 10px 0;
                }
                .post-date{
                    font-size: 12px;
                    color: $tertiary-text-color;
                    >span{
                        color: $green-color;
                    }
                }
                .subtitle{
                    padding: 20px;
                    font-size: 20px;
                }
            }
        }
        .button_1{
            display: inline-block;
            margin-top: 40px;
        }
    }
}
.svg-container{
    display: flex;
    justify-content: center;
}
.template-svg{
    transform: rotate(360deg);
    width: 1200px;
    height: 70px;
}
</style>