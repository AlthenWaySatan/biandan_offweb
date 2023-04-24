<template>
    <div class="background">
        <div class="item">
            <div class="center">
                <img src="/icon.png" alt="icon" class="icon">
                <text class="text_level1 title">便单</text>
                <text class="text_level1 subTitle">小巧轻便的待办清单</text>
            </div>
        </div>
        <div class="item" @mouseover="mouseoverLink" @mouseleave="mouseoutLink" @click="clickLink">
            <text v-if="!Linkstate.show" class="text_level3 itemText">联系我们</text>
            <div v-else class="center">
                <a href="mailto:althenwaysatan@outlook.com" class="text_level3 linkText">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="svgIcon">
                        <path
                            d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z" />
                    </svg>
                    <text>althenwaysatan@outlook.com</text>
                </a>
                <a href="https://jq.qq.com/?_wv=1027&k=8F2h9rxP" class="text_level3 linkText" style="margin-top: 20px;">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="svgIcon">
                        <path
                            d="M433.754 420.445c-11.526 1.393-44.86-52.741-44.86-52.741 0 31.345-16.136 72.247-51.051 101.786 16.842 5.192 54.843 19.167 45.803 34.421-7.316 12.343-125.51 7.881-159.632 4.037-34.122 3.844-152.316 8.306-159.632-4.037-9.045-15.25 28.918-29.214 45.783-34.415-34.92-29.539-51.059-70.445-51.059-101.792 0 0-33.334 54.134-44.859 52.741-5.37-.65-12.424-29.644 9.347-99.704 10.261-33.024 21.995-60.478 40.144-105.779C60.683 98.063 108.982.006 224 0c113.737.006 163.156 96.133 160.264 214.963 18.118 45.223 29.912 72.85 40.144 105.778 21.768 70.06 14.716 99.053 9.346 99.704z" />
                    </svg>
                    <text>798942683</text>
                </a>
            </div>
        </div>
        <div class="item">
            <text class="text_level3 itemText">常见问题</text>
        </div>
        <div class="item">
            <text class="text_level3 itemText">用户协议</text>
        </div>
        <div class="item">
            <text class="text_level3 itemText">隐私声明</text>
        </div>
    </div>
</template>

<script>
import { reactive } from 'vue'
import './footer.css';
import '../HMSansFont.css';
var Linkstate = reactive({ show: false })

export default {
    methods: {
        mouseoverLink() {
            Linkstate.show = true
        },
        mouseoutLink() {
            Linkstate.show = false
        },
        clickLink() {
            Linkstate.show = !Linkstate.show
        }
    },
    setup() {
        return {
            Linkstate
        }
    }
};
</script>