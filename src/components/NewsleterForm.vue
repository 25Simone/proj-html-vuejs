<template>
    <div class="container-fluid">
        <div class="row">
            <div class="form">
                <h1 class="title">Sign up to our Newsletter</h1>
                <input type="text">
                <div class="button_1">Subscribe</div>
                <p class="subtitle">(We do not share your data with anybody, and only use it for its intended purpose)</p>
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

.container-fluid{
    background: url('../assets/images/newsletter_background.jpg');
    background-size: cover;
    .row{
        padding: 50px;
        justify-content: center;
        align-items: center;
        >div{
            width: 600px;
            display: flex;
            flex-direction: column;
            .title{
                text-align: center;
                padding: 30px;
            }
            input{
                width: 100%;
                height: 50px;
                border-radius: 10px;
                border: 1px solid $tertiary-text-color;
            }
            .button_1{
                margin: 30px 0;
            }
            .subtitle{
                text-align: center;
            }
        }
    }
}
</style>