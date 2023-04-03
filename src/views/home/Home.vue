<template>
    <div class="home">
        <home-nav-bar />
        <div class="banner">
            <img src="@/assets/images/home/banner.webp" alt="">
        </div>
        <div class="location">
            <div class="city">广州</div>
            <div class="position">
                <span class="text">我的位置</span>
                <img src="@/assets/images/home/icon_location.png" alt="">
            </div>
        </div>
    </div>
</template>

<script setup>
    import homeNavBar from './cpns/home-nav-bar.vue';
</script>
<style lang="less" scoped>
    .banner {
        img {
            width: 100%;
        }
    }
    .location {
        padding: 2rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .city {
            font-size: 1.6rem;
        }
        .position {
            display: flex;
            align-items: center;
            .text {
                font-size: 1.2rem;
                margin-right: .5rem;
            }
            img {
                width: 2rem;
            }
        }
    }
</style>