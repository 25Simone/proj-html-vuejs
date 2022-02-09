<template>
    <footer class="container-fluid">
        <div class="container">
            <div class="row">
                <div class="footer-col">
                    <img class="img-fluid" src="@/assets/images/avada-drivers-logo-2x-200x39.png" alt="logo">
                    <p>Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wannting to pass first time.</p>
                </div>
                <!-- CONTACT -->
                <div class="footer-col">
                    <label>CONTACT DETAILS</label>
                    <ul class="list-style-reset">
                        <li v-for="contact in contacts" :key="contact.id">
                            <i :class="contact.fa_icon"></i>
                            {{contact.text}}
                        </li>
                    </ul>
                </div>
                <!-- COURSES -->
                <div class="footer-col">
                    <label>COURSES</label>
                    <ul class="list-style-reset" id="courses-links">
                        <li v-for="courseLink in coursesLinks" :key="courseLink.id">
                            <i class="far fa-arrow-alt-circle-right"></i>
                            {{courseLink.name}}
                        </li>
                    </ul>
                </div>
                <!-- FOOTER AD -->
                <div class="footer-col" id="footer-ad">
                    <img class="img-fluid" src="@/assets/images/footer-ad-grid.png" alt="footer ad image">
                    <div class="button_1">BOOK NOW</div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    props: {
        contacts: Array,
        coursesLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

footer{
    background: url('../assets/images/footer-background-color.jpg') center;
    background-size: cover;
    padding: 60px 0;
    .footer-col{
        width: calc(100% / 4);
        padding: 0 25px;
        p{
            color: $tertiary-text-color;
            line-height: 30px;
            font-size: 14px;
        }
        label{
            color: $primary-text-color;
            font-weight: bold;
        }
        ul{
            color: $tertiary-text-color;
            li{
                margin: 20px 0;
                font-size: 14px;
                i{
                    margin-right: 15px;
                }
            }
        }
        #courses-links li{
            font-size: 18px;
            color: $green-color;
            cursor: pointer;
        }

    }
    #footer-ad{
        text-align: center;
        .button_1{
            display: inline-block; 
            font-weight: bold;
            margin: 15px 0;   
        }
    }
}
</style>