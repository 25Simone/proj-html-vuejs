<template>
    <div class="container-fluid pre-header">
        <div class="container">
            <div class="row">
                <p>We have a 95% Successful Pass Rate!</p>
                <p> <i class="fas fa-phone"></i> Give us a call to book your tuition! 1-800-555-555</p>
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

.pre-header{
    background: $secondary-text-color;
    color: $tertiary-text-color;
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