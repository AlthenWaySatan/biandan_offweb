<template>
    <div class="pageback" style="background-color: #F7B500;">
        <div class="pageback_img1 align_center move-insideout">
            <img v-if="!isMobile" src="/background/4.svg" alt="background" class="pageback_img_center_1">
            <img v-else src="/background/4.svg" alt="background" class="pageback_img_center_1-m">
        </div>
        <div class="pageback_img2 align_center move-insideout">
            <img v-if="!isMobile" src="/background/4.svg" alt="background" class="pageback_img_center_2">
            <img v-else src="/background/4.svg" alt="background" class="pageback_img_center_2-m">
        </div>
        <div v-if="!isMobile" class="center1 fade-in">
            <div class="centerIntorPage4">
                <div class="textAreaPage4 setLeft_Buttom">
                    <text class="text_level1 pageIntorTitle">·大屏适配</text>
                    <text class="text_level1 pageIntorText">
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                        平板折叠屏界面同步开发，完美适配大屏，为您带来更舒适的沉浸式体验。
                    </text>
                </div>
                <img src="/pageImg/pageImg4.png" class="pageImg4">
                <div class="textAreaPage4 setRight_Top">
                    <text class="text_level1 pageIntorTitle">·多端同步</text>
                    <text class="text_level1 pageIntorText">
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                        开启多端同步后，应用数据可在您的不同设备间自动同步，让您在随时随地进入状态。
                    </text>
                </div>
            </div>
        </div>
        <div v-else class="center1 fade-in">
            <div class="centerIntorPage4">
                <div class="textAreaPage4-m-1 setLeft_Buttom-m">
                    <text class="text_level1 pageIntorTitle-m">·大屏适配</text>
                    <text class="text_level1 pageIntorText-m">
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                        平板折叠屏界面同步开发，完美适配大屏，为您带来更舒适的沉浸式体验。
                    </text>
                </div>
                <img src="/pageImg/pageImg4-m.png" class="pageImg4-m">
                <div class="textAreaPage4-m-2 setRight_Top-m">
                    <text class="text_level1 pageIntorTitle-m">·多端同步</text>
                    <text class="text_level1 pageIntorText-m">
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                        开启多端同步后，应用数据可在您的不同设备间自动同步，让您在随时随地进入状态。
                    </text>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import './page4.css';
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