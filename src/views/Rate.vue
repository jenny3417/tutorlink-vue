<template>
    <navbar></navbar>
    <div class="container scorePage">
        <h1>好評推薦</h1>
        <div class="scoreContent">
            <div class="card mb-3" style="max-width: 100%;" v-for="data in 12">
                <div class="row g-0">
                    <div class="col-md-3">
                        <img src="https://fakeimg.pl/350x180/" class="img-fluid rounded-start" alt="...">
                    </div>
                    <div class="col-md-9">
                        <div class="card-body p-3">
                            <h3 class="card-title"> data.lesson.lessonName <span class="scoreDate">2023/8/24</span><span
                                    v-for="rating in 5 " :key="rating" class="rateStyle">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="gold"
                                        class="bi bi-star-fill" viewBox="0 0 16 16">
                                        <path
                                            d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.282.95l-3.522 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z" />
                                    </svg>
                                </span></h3>
                            <!-- 這門課程深入挖掘了現代文學的精髓，讓我對各種文學流派有更深入的理解。教授充滿激情，引導我們探索不同作品背後的意義，雖然有時候閱讀量稍大，但收穫良多。 -->
                            <p class="card-text"> data.rateContent
                            </p>
                            <p class="card-text text-end"> data.users.userAccount </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 新增評分的按鈕 -->
    <score-edit></score-edit>

    <!-- 新增檢舉的按鈕 -->
    <report-button></report-button>
</template>
    
<script setup>

import navbar from "@/components/public/Navbar.vue"
import scoreEdit from "../components/score/ScoreEdit.vue";
import ReportButton from "../components/report/ReportButton.vue";
import { ref } from "vue"
import tutorlink from '../api/tutorlink'

const ratings = ref(5)
// const datas = ref([])

// const fetchData = async () => {
//     try {
//         const response = await tutorlink.get("/favoriate");
//         datas.value = response.data
//     } catch (error) {
//         console.error('Error fetching data:', error);
//     }
// };

// fetchData()

</script>
    
<style scoped>
.scoreDate {
    font-size: 18px;
    margin-left: 20px;
    margin-right: 20px;
}

.selected {
    color: gold;
}

.rateStyle {
    margin: 2px;
}
</style>