<template>
    <div class="background">
        <div class="items">
            <div class="item">
                <a href="#/" class="text_level1">
                    <div class="center fade-in">
                        <img src="/icon.png" alt="icon" class="icon">
                        <text v-if="!isMobile" class="title">便单</text>
                        <text v-if="!isMobile" class="subTitle">小巧轻便的待办清单</text>
                    </div>
                </a>
            </div>
            <div class="item" @mouseover="showLink" @mouseleave="hideLink" @click="showLink" ref="target">
                <text v-if="!Linkstate.show && isMobile" class="text_level3 itemText-m fade-in">联系<br>我们</text>
                <text v-else-if="!Linkstate.show && !isMobile" class="text_level3 itemText fade-in">联系我们</text>
                <div v-else-if="Linkstate.show && isMobile" class="center linkArea fade-in" id="needOut">
                    <myLink></myLink>
                </div>
                <div v-else-if="Linkstate.show && !isMobile" class="center fade-in">
                    <myLink></myLink>
                </div>
            </div>
            <div class="item">
                <a href="#/questions" class="text_level3">
                    <text v-if="isMobile" class="itemText-m fade-in">常见<br>问题</text>
                    <text v-else class="itemText fade-in">常见问题</text>
                </a>
            </div>
            <div class="item">
                <a href="#/userAgreement" class="text_level3">
                    <text v-if="isMobile" class="itemText-m fade-in">用户<br>协议</text>
                    <text v-else class="itemText fade-in">用户协议</text>
                </a>
            </div>
            <div class="item">
                <a href="#/privacyStatement" class="text_level3">
                    <text v-if="isMobile" class="itemText-m fade-in">隐私<br>政策</text>
                    <text v-else class="itemText fade-in">隐私政策</text>
                </a>
            </div>
        </div>
        <div class="links">
            <a href="https://beian.miit.gov.cn" class="text_level3 linkText">
                备案号：苏ICP备2025173909号-1
            </a>
        </div>
    </div>
</template>

<script>
import { reactive } from 'vue'
import { ref } from 'vue'
import { onClickOutside } from '@vueuse/core'
import myLink from '../element/myLink.vue'
import './footer.css';
import '../HMSansFont.css';
var Linkstate = reactive({ show: false })

export default {
    components: {
        myLink
    },
    methods: {
        showLink() {
            console.log('showLink')
            Linkstate.show = true
        },
        hideLink() {
            console.log('hideLink')
            Linkstate.show = false
        }
    },
    computed: {
        isMobile() {
            return window.matchMedia("(max-width: 600px)").matches;
        }
    },
    setup() {
        const target = ref(null)

        onClickOutside(target, (event) => {
            if (!Linkstate.show) return;
            document.getElementById("needOut").classList.add('fade-out')
            setTimeout(function () {
                Linkstate.show = false
            }, 800)
        })
        return {
            Linkstate,
            target
        }
    }
};
</script>