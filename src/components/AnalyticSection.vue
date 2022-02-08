<template>
    <div class="container-fluid">
        <img class="" src="@/assets/svg/driving-triangle.svg" alt="">
        <div class="container">
            <div class="row">
                <div></div>
                <div></div>
                <div></div>
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
    >img{
        transform: rotate(360deg);
        height: 150px;
        width: 100%;
        margin-top: -2px;
    }
    .container{
        position: relative;
        top: -150px;
        .row{
            >div{
                width: calc(100% / 3 - 10px);
                margin: 0 5px;
                border-top: 4px solid $green-color;
                border-radius: 10px;
                background: #fff;
                box-shadow: 5px 10px 18px #888888;
                height: 350px; // reference
            }
        }
    }
}
</style>