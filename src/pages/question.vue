<template>
    <div class="textBack">
        <div class="textArea fade-in">
            <div class="titleArea">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" version="1.1" class="titleIcon">
                    <path
                        d="M12,1 C18.0751322,1 23,5.92486775 23,12 C23,18.0751322 18.0751322,23 12,23 C5.92486775,23 1,18.0751322 1,12 C1,5.92486775 5.92486775,1 12,1 Z M12,16.5 C11.44775,16.5 11,16.94775 11,17.5 C11,18.05225 11.44775,18.5 12,18.5 C12.55225,18.5 13,18.05225 13,17.5 C13,16.94775 12.55225,16.5 12,16.5 Z M12.6929199,6.06634025 C10.4971863,5.64561935 8.5,7.28866322 8.5,9.46493686 C8.5,9.87915043 8.83578644,10.2149369 9.25,10.2149369 C9.66421356,10.2149369 10,9.87915043 10,9.46493686 C10,8.23197222 11.1380704,7.29570522 12.4104462,7.53950302 C13.1835078,7.68784166 13.8115486,8.30785305 13.9604236,9.06493852 C14.1456712,10.0065105 13.6538963,10.9002855 12.7993629,11.2668006 C11.8501216,11.673853 11.2501432,12.6306191 11.2501432,13.6716862 L11.2501432,13.6716862 L11.2501432,14.25 C11.2501432,14.6642136 11.5859296,15 12.0001432,15 C12.4143567,15 12.7501432,14.6642136 12.7501432,14.25 L12.7501432,14.25 L12.7501432,13.6716862 C12.7501432,13.2176189 13.0054203,12.8105368 13.390581,12.6453727 C14.8855687,12.0041625 15.7561549,10.4219179 15.4322233,8.77544644 C15.1648814,7.41591203 14.0644076,6.32950759 12.6929199,6.06634025 Z" />
                </svg>
                <text class="text_level1 titleText">常见问题解答</text>
                <text class="text_level1 subTitleText">更新时间：2023年6月23日</text>
            </div>
            <div v-for="item in data" class="questionArea">
                <text class="text_level1 questionText">
                    {{ item.Question }}
                </text>
                <div class="answerArea">
                    <text v-for="ans in item.Answer" class="text_level1 answerText">
                        {{ ans }}
                    </text>
                </div>
            </div>
        </div>
        <div class="footer bottom">
            <Footer></Footer>
        </div>
    </div>
</template>
<script>
import Footer from "../views/footer.vue";
import '../style.css';
import '../animate.css';
import './question.css';
import QuestionData from "../json/QuestionAndAnswer.json"

export default {
    components: {
        Footer
    },
    data() {
        return {
            data: QuestionData
        }
    }
};
</script>
  