<template>
    <div class="container-fluid">
        <div class="container">
            <div class="row">
                <div>
                    <h1>Start Learning to Drive Today</h1>
                    <p>Give us a call to schedule your first driving lesson</p>
                </div>
                <div id="phone"> <i class="fas fa-phone"></i> {{phone}}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        phone: String,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.container-fluid{
    background: url('../assets/images/horizontal-cta-background.jpg');
    background-size: cover;
    .container{
        padding: 80px 0;
        color: $primary-text-color;
        .row{
            justify-content: space-between;
            align-items: center;
            #phone{
                font-size: 30px;
            }
            h1{
                font-size: 40px;
                margin-bottom: 20px;
            }
            p{
                font-size: 20px;
            }
        }
    }
}
</style>