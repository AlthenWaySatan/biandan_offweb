<template>
    <div class="pageback">
        <div class="pageback_img1 align_center move-outsidein">
            <img src="/background/3-1.webp" alt="background" class="pageback_img_center">
        </div>
        <div class="pageback_img2 align_center move-outsidein">
            <img src="/background/3-0.5.webp" alt="background" class="pageback_img_center">
        </div>
        <div v-if="!isMobile" class="center1 fade-in">
            <div class="pageTextArea">
                <text class="text_level1 pageIntorTitle">·多种颜色主题，打造个性化界面</text>
                <text class="text_level1 pageIntorText">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    便单应用内提供便单黄，宇宙蓝，燃力红，樱花粉等6种不同的颜色，满足您的个性化需求，打造彰显自我个性的便单。
                </text>
                <div style="width: 100%; height: 120px;"></div>
                <text class="text_level1 pageIntorTitle">·适配系统深色，享受沉浸式体验</text>
                <text class="text_level1 pageIntorText">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    根据系统深浅自动适配深色浅色，白天看得清，晚上不瞎眼；和系统界面统一，为您带来更沉浸的体验。
                </text>
            </div>
            <div class="pageImgArea">
                <SkinSwiper></SkinSwiper>
            </div>
        </div>
        <div v-else class="center1 fade-in">
            <div class="pageTextArea-m">
                <text class="text_level1 pageIntorTitle-m">·多种颜色主题，打造个性化界面</text>
                <text class="text_level1 pageIntorText-m">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    便单应用内提供便单黄，宇宙蓝，燃力红，樱花粉等6种不同的颜色，满足您的个性化需求，打造彰显自我个性的便单。
                </text>
                <div style="width: 100%; height: 24px;"></div>
                <text class="text_level1 pageIntorTitle-m">·适配系统深色，享受沉浸式体验</text>
                <text class="text_level1 pageIntorText-m">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    根据系统深浅自动适配深色浅色，白天看得清，晚上不瞎眼；和系统界面统一，为您带来更沉浸的体验。
                </text>
            </div>
            <div class="pageImgArea-m">
                <SkinSwiper_m></SkinSwiper_m>
            </div>
        </div>
    </div>
</template>

<script>

import './page3.css';
import '../HMSansFont.css';
import '../animate.css';

import SkinSwiper from "../element/skinSwiper.vue";
import SkinSwiper_m from "../element/skinSwiper-m.vue";

export default {
    components: {
        SkinSwiper,
        SkinSwiper_m,
    },
    computed: {
        isMobile() {
            return window.matchMedia("(max-width: 600px)").matches;
        }
    },
    setup() {
    }
};
</script>