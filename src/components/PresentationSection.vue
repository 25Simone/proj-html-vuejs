<template>
    <div class="container">
        <div class="row">
            <div id="section-left">
                <h1>Get Behind The Wheel</h1>
                <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.</p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper. Fusce et ulceris libero, at suscipit lacus. Sed viate fringilla nibh. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis vehicula semper. Fusce et ultrices libero, at suscipit lacus. Sed viate fringilla nibh.</p>
            </div>
            <div id="first-lesson-tab">
                <div class="box-shadow">
                    <h1>First Lesson Free!</h1>
                    <p>When you make a block booking with us your first lesson is included free.</p>
                    <form>
                        <img src="@/assets/images/image.png" alt="">
                        <input type="text" placeholder="Your Name*">
                        <input type="text" placeholder="Email*">
                        <input type="text" placeholder="Telephone">
                        <input type="text" placeholder="Location">
                        <div class="button_1">REQUEST A CALLBACK</div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.container{
    padding-bottom: 80px;
}
.row{
    >div{
        max-width: 50%;
    }
    p{
        color: $tertiary-text-color;
        line-height: 30px;
    }
    #section-left{
        padding: 50px 40px;
        h1{
            font-size: 40px;
            color: $secondary-text-color;
            margin: 40px 0;
        }
        .subtitle{
            font-size: 22px;
            line-height: 45px;
            margin-bottom: 30px;
        }
    }
    #first-lesson-tab{
        margin-top: -5%;
        width: 100%;
        >div{
            background: #fff;
            width: 100%;
            border-radius: 10px;
            padding: 50px 40px;
            text-align: center;
            h1{
                color: $green-color;
                margin-bottom: 20px;
            }
            p{
                padding: 30px 0;
            }
            form{
                position: relative;
                >img{
                    width: 20px;
                    position: absolute;
                    top: 32px;
                    right: 15px;
                }
            }
            input{
                width: 100%;
                margin: 20px 0;
                padding: 0 15px;
                height: 45px;
                border: 1px solid $tertiary-text-color;
                border-radius: 5px;
                background: #f7f7f7;
                color: $tertiary-text-color;
            }
            .button_1{
                display: inline-block;
                font-weight: bold;
                margin: 10px 0;
            }
        }
    }
}
</style>