<template>
    <div class="container">
        <div class="row">
            <div id="section-left">
                <h1>Get Behind The Wheel</h1>
                <p id="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.</p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula semper. Fusce et ulceris libero, at suscipit lacus. Sed viate fringilla nibh. Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis vehicula semper. Fusce et ultrices libero, at suscipit lacus. Sed viate fringilla nibh.</p>
            </div>
            <div id="first-lesson-tab">
                <div>
                    <h1>First Lesson Free!</h1>
                    <p>When you make a block booking with us your first lesson is included free.</p>
                    <form>
                        <input type="text">
                        <input type="text">
                        <input type="text">
                        <input type="text">
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
        #subtitle{
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
            box-shadow: 5px 10px 18px #888888;
            h1{
                color: $green-color;
                margin-bottom: 20px;
            }
            p{
                padding: 30px 0;
            }
            input{
                width: 100%;
                margin: 20px 0;
                height: 40px;
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