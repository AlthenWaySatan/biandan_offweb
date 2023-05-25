<template>
    <div class="pageback">
        <div class="pageback_img1 align_left move-left">
            <img src="/background/1-1-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img1 align_right move-right">
            <img src="/background/1-1-r.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_left move-left">
            <img src="/background/1-0.5-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_right move-right">
            <img src="/background/1-0.5-r.svg" alt="background" class="pageback_img">
        </div>
        <div v-if="!isMobile" class="center1 fade-in">
            <div class="pageImgArea">
                <img src="/pageImg/pageImg1.png" alt="pageImg1" class="pageImg">
            </div>
            <div class="pageTextArea">
                <text class="text_level1 pageIntorTitle">·ArkTS语言，打造原生体验</text>
                <text class="text_level1 pageIntorText">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    采用ArkTS语言编写，便单APP占用空间超小，仅需10MB不到的空间即可安装；基于ArkUI的强大能力和原生图标的精确使用，
                    我们创建了简洁明了的设计风格，让您一目了然地看到自己的任务清单。
                </text>
                <div style="width: 100%; height: 120px;"></div>
                <text class="text_level1 pageIntorTitle">·学习工作生活，一切尽在掌握</text>
                <text class="text_level1 pageIntorText">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    自定义创建待办单分类，会在事项前用颜色注明，不同事项轻松分类；三种不同图标对应三种不同的完成状态：待完成，正在完成，
                    已完成，让您轻松获取当前状态。
                </text>
            </div>
        </div>
        <div v-else class="center1 fade-in">
            <div class="pageImgArea-m">
                <img src="/pageImg/pageImg1.png" alt="pageImg1" class="pageImg-m">
            </div>
            <div class="pageTextArea-m">
                <text class="text_level1 pageIntorTitle-m">·ArkTS语言，<br>打造原生体验</text>
                <text class="text_level1 pageIntorText-m">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    采用ArkTS语言编写，便单APP占用空间超小，仅需10MB不到的空间即可安装；基于ArkUI的强大能力和原生图标的精确使用，
                    我们创建了简洁明了的设计风格，让您一目了然地看到自己的任务清单。
                </text>
                <div style="width: 100%; height: 24px;"></div>
                <text class="text_level1 pageIntorTitle-m">·学习工作生活，<br>一切尽在掌握</text>
                <text class="text_level1 pageIntorText-m">
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    自定义创建待办单分类，会在事项前用颜色注明，不同事项轻松分类；三种不同图标对应三种不同的完成状态：待完成，正在完成，
                    已完成，让您轻松获取当前状态。
                </text>
            </div>
        </div>
    </div>
</template>

<script>

import './page1.css';
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