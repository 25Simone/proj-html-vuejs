<template>
    <div class="container">
        <div class="row">
            <!-- ANALYTICS ITEMS -->
            <div
            class="box-shadow"
            v-for="(item, i) in items"
            :key="i"
            >
                <div class="analytic-date">
                    {{item.value}}
                    <!-- LOADER SVG -->
                    <svg v-if="item.show_id != 0" height="230" width="230">
                        <circle :class="`circle-${item.show_id}`" cx="110" cy="110" r="105" />
                    </svg>
                </div>
                <h3 id="rate-name">{{item.rate_name.toUpperCase()}}</h3>
            </div>
        </div> 
    </div>
</template>

<script>
export default {
    props: {
        items: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.container{
    .row{
        >div{
            width: calc(100% / 3 - 16px);
            margin: 0 8px;
            padding: 50px;
            border-top: 4px solid $green-color;
            border-radius: 10px;
            background: #fff;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: all .5s;
            &:hover{
                transform: scale(1.1);
            }
            .analytic-date{
                width: 220px;
                height: 220px;
                border-radius: 50%;
                border: 10px solid #ccc;
                display: flex;
                align-items: center;
                justify-content: center;
                position: relative;
                color: $tertiary-text-color;
                font-size: 50px;
                svg{
                    position: absolute;
                    top: -10px;
                    left: -10px;
                    z-index: 5
                }
                circle {
                    fill: transparent;
                    stroke: $green-color;
                    stroke-width: 11;
                }
                .circle-95{
                    stroke-dasharray: 810;
                    stroke-dashoffset: 180;
                }
            }
            #rate-name{
                color: $tertiary-text-color;
                padding: 40px 0;
            }
            
        }
    }
}
</style>