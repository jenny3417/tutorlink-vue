<template>
    <div class="content-with-loading card-body">
        <div class="cart-item-row row divider-line">
            <!-- 主圖＋介紹-->
            <div class="col-12 col-lg-6 px-2 px-lg-3">
                <div class="main d-flex">
                    <!-- 課程圖片 -->
                    <div class="cart-item-image">
                        <a href="/product/1001112702764163" class="" title="課程名稱" target="_self">
                            <img src="https://fakeimg.pl/250x150/" alt="image">
                        </a>
                    </div>
                    <!-- 課程名稱 -->
                    <div class="cart-item-description ps-3">
                        <a href="/product/1001112702764163" class="" title="課程名稱" target="_self">
                            <span class="product-name fw-bold">N5日文文法</span>
                        </a>
                    </div>
                </div>
            </div>
            <!-- 課程類型 -->
            <div class="offset-8 offset-lg-0 col-4 col-lg-2 p-0 text-lg-center text-end my-auto pe-2 pe-lg-0 pt-2 pt-lg-0">
                <span class="cart-price-black">影音課程</span>
            </div>
            <!-- 課程數量 -->
            <div class="align-self-center col-8 col-lg-2 p-0 margin-top text-lg-center">
                10堂
            </div>
            <!-- 小計 -->
            <div class="col-4 p-0 margin-top text-end my-auto pe-2 pe-lg-0 col-lg-1 text-lg-center">
                $261
            </div>
            <!-- 退費 -->
            <div class="offset-8 offset-lg-0 col-4 col-lg-1 p-0 text-end my-auto pe-2 pe-lg-0 pt-2 pt-lg-0 text-lg-center">
                <button class="btn btn-outline-primary my-1" type="button" data-bs-toggle="modal"
                    data-bs-target="#exampleModal">查看上課時間</button>
                <!-- 退費彈出視窗 -->
                <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel"
                    aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h5 class="modal-title" id="exampleModalLabel">上課時間</h5>
                                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <!-- 退費彈出視窗內容 -->
                            <div class="modal-body">
                                這裡放日歷
                            </div>
                            <!-- 彈出視窗的確認 -->
                            <div class="modal-footer">
                                <button type="button" class="btn btn-primary" data-bs-dismiss="modal">確認</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <n-divider />
</template>
<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
    setup() {
        return {
            value: ref(0)
        }
    }
});
</script>

<style scoped>
.n-divider {
    margin: 1px;
}
</style>