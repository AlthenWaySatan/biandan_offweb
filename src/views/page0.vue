<template>
    <div class="pageback">
        <div class="pageback_img1 align_left move-left">
            <img src="/background/0-1-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img1 align_right move-right">
            <img src="/background/0-1-r.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_left move-left">
            <img src="/background/0-0.5-l.svg" alt="background" class="pageback_img">
        </div>
        <div class="pageback_img2 align_right move-right">
            <img src="/background/0-0.5-r.svg" alt="background" class="pageback_img">
        </div>
        <div v-if="!isMobile" class="center0 fade-in">
            <img src="/icon.png" alt="icon" class="mainIcon">
            <text class="text_level1 mainTitle">便单</text>
            <text class="text_level1 mainSubTitle">小巧轻便的待办清单</text>
            <text class="text_level3 mainIntroduce">
                · ArkTS 原生打造 · 5MB超小空间 · <br>
                · 多端同步 · 本地备份 · <br>
                · 四象限视图 · 日历视图· <br>
                · 多彩主题 · 自动深色 ·
            </text>
            <a
                href="hiapplink://com.huawei.appmarket?appId=C1005682483720629056&channelId=%E5%AE%98%E7%BD%91&id=99ec639f5dc248f1954be6589dbdebff&s=45B9CCD9D797BF5DFC6FE018B42AC7CEDCE08E3684092E47C3EC1266BD85AB3E&detailType=0&v=&callType=AGDLINK&installType=0000">
                <div class="mainStamp"></div>
            </a>
        </div>
        <div v-else class="center0 fade-in">
            <img src="/icon.png" alt="icon" class="mainIcon-m">
            <text class="text_level1 mainTitle-m">便单</text>
            <text class="text_level1 mainSubTitle-m">小巧轻便的待办清单</text>
            <text class="text_level3 mainIntroduce-m">
                · ArkTS 原生打造 · 5MB超小空间 · <br>
                · 多端同步 · 本地备份 · <br>
                · 四象限视图 · 日历视图· <br>
                · 多彩主题 · 自动深色 ·
            </text>
            <a
                href="hiapplink://com.huawei.appmarket?appId=C1005682483720629056&channelId=%E5%AE%98%E7%BD%91&id=99ec639f5dc248f1954be6589dbdebff&s=45B9CCD9D797BF5DFC6FE018B42AC7CEDCE08E3684092E47C3EC1266BD85AB3E&detailType=0&v=&callType=AGDLINK&installType=0000">
                <div class="mainStamp"></div>
            </a>
        </div>
    </div>
</template>

<script>

import './page0.css';
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