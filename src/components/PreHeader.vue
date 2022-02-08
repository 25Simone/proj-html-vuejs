<template>
    <div class="container-fluid pre-header">
        <div class="container">
            <div class="row">
                <p>We have a 95% Successful Pass Rate!</p>
                <p> <i class="fas fa-phone"></i> Give us a call to book your tuition! {{phone}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        phone: String,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.pre-header{
    background: #333;
    color: $tertiary-text-color;
    position: fixed;
    top: 0;
    .container{
        padding: 15px 0;
        .row{
            justify-content: space-between;
            font-size: 12px;
            i{
                margin-right: 10px;
            }
        }
    }
}
</style>