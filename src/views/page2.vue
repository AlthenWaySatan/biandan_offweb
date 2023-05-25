<template>
    <div class="pageback">
        <div class="pageback_img1 align_left move-left">
            <img src="/background/2-1-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img1 align_right move-right">
            <img src="/background/2-1-r.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_left move-left">
            <img src="/background/2-0.5-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_right move-right">
            <img src="/background/2-0.5-r.svg" alt="background" class="pageback_img">
        </div>
        <div v-if="!isMobile" class="center1 fade-in">
            <div class="centerIntor">
                <div class="halfPart">
                    <div class="pageImgArea-2">
                        <img src="/pageImg/pageImg2-1.png" alt="pageImg2-1" class="pageImg">
                    </div>
                    <div style="width: 100%;height: 24px;"></div>
                    <div class="pageTextArea">
                        <text class="text_level1 pageIntorTitle">·日历视图，事项尽收眼底</text>
                        <text class="text_level1 pageIntorText">
                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                            打开日历视图，可以快捷浏览该月的所有事项，左右滑动切换月份，点击可以查看具体日期。
                        </text>
                    </div>
                </div>
                <div class="halfPart">
                    <div class="pageTextArea">
                        <text class="text_level1 pageIntorTitle">·ArkTS语言，打造原生体验</text>
                        <text class="text_level1 pageIntorText">
                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                            打开四象限视图，便单将会根据您给的信息自动将今天的事项填入四象限，方便您安排事项的完成顺序。
                        </text>
                    </div>
                    <div style="width: 100%;height: 24px;"></div>
                    <div class="pageImgArea-2">
                        <img src="/pageImg/pageImg2-2.png" alt="pageImg2-2" class="pageImg">
                    </div>
                </div>
            </div>
        </div>
        <div v-else class="center1 fade-in">
            <div class="centerIntor">
                <div class="halfPart-m">
                    <div class="pageImgArea-2-m">
                        <img src="/pageImg/pageImg2-1.png" alt="pageImg2-1" class="pageImg-m">
                    </div>
                    <div style="width: 100%;height: 24px;"></div>
                    <div class="pageTextArea-2-m">
                        <text class="text_level1 pageIntorTitle-m">·日历视图，<br>事项尽收眼底</text>
                        <text class="text_level1 pageIntorText-m">
                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                            打开日历视图，可以快捷浏览该月的所有事项，左右滑动切换月份，点击可以查看具体日期。
                        </text>
                    </div>
                </div>
                <div class="halfPart-m">
                    <div class="pageTextArea-2-m">
                        <text class="text_level1 pageIntorTitle-m">·ArkTS语言，<br>打造原生体验</text>
                        <text class="text_level1 pageIntorText-m">
                            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                            打开四象限视图，便单将会根据您给的信息自动将今天的事项填入四象限，方便您安排事项的完成顺序。
                        </text>
                    </div>
                    <div style="width: 100%;height: 24px;"></div>
                    <div class="pageImgArea-2-m">
                        <img src="/pageImg/pageImg2-2.png" alt="pageImg2-2" class="pageImg-m">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import './page2.css';
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