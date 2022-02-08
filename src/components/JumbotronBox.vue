<template>
    <div class="container-fluid">
        <div class="jumbo-txt container">
            <h1>Drive with Avada</h1>
            <p>We offer the finest driving tuition money can buy</p>
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
    height: 80vh;
    background: url('../assets/images/homepage-hero-background.jpg');
    background-size: cover;
    background-position: center;
    .jumbo-txt{
        color: $primary-text-color;
        padding-top: 40vh;
        >h1 {
            font-size: 60px;
            margin-bottom: 20px;
        }
        >p{
            font-size: 25px;
        }
    }
}
</style>