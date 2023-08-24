<template>
    <div class="pageback">
        <div v-if="!isMobile" class="pageback_img1 move-up">
            <img src="/background/5-1-u.svg" alt="background" class="pageback_img5">
        </div>
        <div v-else class="pageback_img2 move-up" style="width: 220%;">
            <img src="/background/5-1-u.svg" alt="background" class="pageback_img5">
        </div>
        <div class="pageback_img1 move-done">
            <div style="position: relative; height: 100%; width: 100%;">
                <img v-if="!isMobile" src="/background/5-1-d.svg" alt="background" class="pageback_img5 align_done"
                    style="width: 50%;">
                <img v-else src="/background/5-1-d.svg" alt="background" class="pageback_img5 align_done"
                    style="width: 110%;">
            </div>
        </div>
        <div v-if="!isMobile" class="pageback_img2 move-up">
            <img src="/background/5-0.5-u.svg" alt="background" class="pageback_img5">
        </div>
        <div v-else class="pageback_img2 move-up" style="width: 220%;">
            <img src="/background/5-0.5-u.svg" alt="background" class="pageback_img5">
        </div>
        <div class="pageback_img2 move-done">
            <div style="position: relative; height: 100%; width: 100%;">
                <img v-if="!isMobile" src="/background/5-0.5-d.svg" alt="background" class="pageback_img5 align_done"
                    style="width: 70%;">
                <img v-else src="/background/5-0.5-d.svg" alt="background" class="pageback_img5 align_done"
                    style="width: 154%;">
            </div>
        </div>
        <div v-if="!isMobile" class="center5">
            <div class="center1 align_done fade-sidewaysIn" style="height: 80%; width: 100;">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%; transform: translate(12%, 18.75%);">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%;">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%; transform: translate(-12%, -18.75%);">
            </div>
            <div class="pageTextArea5 fade-in">
                <text class="text_level1 pageIntorTitle">·六款万能卡片，操作一步到位</text>
                <text class="text_level1 pageIntorText">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    提供日历，四象限，待办单，进度环等各种不同功能尺寸的卡片。放置桌面，信息一目了然，操作一步直达。
                </text>
            </div>
        </div>
        <div v-else class="center5">
            <div class="center1 align_done fade-sidewaysIn" style="height: 70%; width: 100; bottom: 10%;">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%; transform: translate(12%, 18.75%);">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%;">
                <img src="/pageImg/pageImg5.webp" alt="pageImg5" style="height: 100%; transform: translate(-12%, -18.75%);">
            </div>
            <div class="pageTextArea5-m fade-in">
                <text class="text_level1 pageIntorTitle-m">·六款万能卡片，操作一步到位</text>
                <text class="text_level1 pageIntorText-m">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    提供日历，四象限，待办单，进度环等各种不同功能尺寸的卡片。放置桌面，信息一目了然，操作一步直达。
                </text>
            </div>
        </div>
    </div>
</template>

<script>

import './page5.css';
import '../HMSansFont.css';
import '../animate.css';

export default {
    computed: {
        isMobile() {
            return window.matchMedia("(max-width: 600px)").matches;
        }
    },
    setup() {
    }
};
</script>