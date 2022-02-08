<template>
    <header class="container-fluid">
        <div class="container">
            <div class="row">
                <div class="logo">
                    <img src="@/assets/images/avada-drivers-logo-1x.png" alt="site logo">
                </div>
                <nav>
                    <ul>
                        <li
                        v-for="item in items"
                        :key="item.id"
                        >
                            {{item.label.toUpperCase()}}
                            <span v-if="item.new_tag" class="new-tag button_1">NEW</span>
                        </li>
                    </ul>
                </nav>
                <div class="button_1">BOOK NOW</div>
            </div>
        </div>
    </header>
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

header{
    background: rgba(73, 76, 78, .5);
    position: fixed;
    top: 44px;
    .container{
        padding: 30px 0;
        .row{
            justify-content: space-between;
            align-items: center;
        }
        nav{
            color: $primary-text-color;
            padding-left: 60px;
            ul{
                list-style: none;
                display: flex;
                align-items: center;
                li{
                    display: flex;
                    align-items: center;
                    font-weight: bold;
                    font-size: 15px;
                    margin: 0 20px;
                    padding: 5px 0;
                    border-bottom: 2px solid transparent;
                    &:hover {
                        color: $green-color;
                        border-color: $green-color;
                    }
                }
                .new-tag.button_1{
                    border-radius: 5px;
                    margin-left: 10px;
                    padding: 4px;
                    font-size: 10px;
                    font-weight: bold;
                }
            }
        }
        .button_1{
            font-weight: bold;
            font-size: 15px;
        }
    }
}
</style>