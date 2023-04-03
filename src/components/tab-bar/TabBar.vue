<template>
    <div class="tab-bar">
        <van-tabbar v-model="currentIndex" active-color="var(--primary-color)">
            <van-tabbar-item 
            v-for="(item, index) in tabbarData" 
            :key="item.text"
            :to="item.path"
            >
                <span>{{ item.text }}</span>
                <template #icon>
                    <img v-if="currentIndex !== index" :src="getAssetUrl(item.image)" alt="">
                    <img v-else :src="getAssetUrl(item.imageActive)" alt="">
                </template>
            </van-tabbar-item>
        </van-tabbar>

        <!-- <template v-for="(item, index) in tabbarData" :key="item.text">
            <div 
            class="tab-bar-item" 
            :class="{ active: index === currentIndex}"
            @click="itemClick(index, item)"
            >
            <img v-if="currentIndex !== index" :src="getAssetUrl(item.image)" alt="">
            <img v-else :src="getAssetUrl(item.imageActive)" alt="">
            <span class="text">{{ item.text }}</span>
        </div>
        </template> -->
    </div>
</template>

<script setup>
    import tabbarData from '@/assets/data/tabbar'
    import getAssetUrl from '@/utils/load_assets'
    import { ref } from 'vue'
    const currentIndex = ref(0);
    

</script>
<style lang="less" scoped>
    .tab-bar {
        img {
            // width: 28px;
            height: 3.6rem;
        }
    }
</style>