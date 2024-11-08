<template>
    <div class="quick-view">
        <div class="quick-view__container">
            <div class="quick-view__header">
                <h3 class="quick-view__title">Xem nhanh</h3>
                <a href="#" class="quick-view__view-all">Xem tất cả</a>
            </div>
            <div class="quick-view__list">
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Infographic: Mùa Mưa Lũ - đề phòng bệnh Hô hấp và
                            bệnh đường Tiêu hóa
                        </a>
                        <img
                            src="../assets/quicknews1.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Infographic: Mùa Mưa Lũ - đề phòng bệnh về Da, Mắt
                            và Sốt xuất huyết
                        </a>
                        <img
                            src="../assets/quicknews2.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Một vài người không dùng sẽ cười Apple để nút nguồn
                            Mac Mini M4 ở mặt đáy
                        </a>
                        <img
                            src="../assets/quickNews3.jpeg"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Tham quan đài thiên văn Griffith Observatory - Nơi
                            Los Angeles chạm tới những vì sao
                        </a>
                        <img
                            src="../assets/quickNew4.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Xiaomi Band 9 Pro ra mắt: Smartband với cạnh viền
                            kim loại, pin 21 ngày, giá từ 1.42 triệu
                        </a>
                        <img
                            src="../assets/quickNews5.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Xiaomi Pad 7 Series ra mắt: 2 phiên bản, tỷ lệ màn
                            hình 3:2, Snapdragon 8s Gen 3, giá từ 7 triệu
                        </a>
                        <img
                            src="../assets/quickNews6.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Final Cut Pro sắp có tính năng tự động tạo phụ đề từ
                            giọng nói
                        </a>
                        <img
                            src="../assets/quickNews7.webp"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
                <div class="quick-view__item">
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a href="#" class="quick-view__link">
                            Xiaomi Watch S4 ra mắt: Thay vòng bezel linh hoạt,
                            pin 15 ngày, giá từ 3.5 triệu
                        </a>
                        <img
                            src="../assets/quicknews8.jpg"
                            alt="News Image"
                            class="quick-view__image"
                        />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "QuickView",
    props: {
        msg: String,
    },
};
</script>

<style scoped>
/* Quick View */
.quick-view {
    width: 350px;
    display: flex;
    flex-direction: column;
    align-self: start;
    padding: 32px 20px 0px 0px;
    /* gap: 10px; */
}

.quick-view__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0px 0px 16px;
}

.quick-view__title,
.featured-articles__title {
    font-weight: bold;
    font-size: 18px;
    color: var(--color-secondary);
}

.quick-view__view-all {
    font-size: 14px;
    color: var(--color-primary);
    text-decoration: none;
}

.quick-view__list {
    position: relative;
    border-left: dotted 1px var(--color-border);
    border-bottom: dotted 1px var(--color-border);
    border-bottom-left-radius: 30px;
    display: flex;
    flex-direction: column;
    padding: 0px 16px 16px;
}

.quick-view__item {
    width: 100%;
    display: flex;
    gap: 10px;
    align-items: center;
    margin: 0px 0px 16px;
}

.quick-view__timeline-dot {
    margin-bottom: 40px;
    position: absolute;
    left: -5px;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: var(--color-primary);
}

.quick-view__content {
    display: flex;
    align-items: center;
}

.quick-view__link {
    width: 165px;
    margin-right: 12px;
    font-size: 14px;
    line-height: 20px;
    font-weight: 700;
    color: var(--color-secondary);
    font-weight: bold;
    text-decoration: none;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}

.quick-view__image {
    width: 120px;
    height: 60px;
    border-radius: 5px;
    object-fit: cover;
}

@media (min-width: 320px) and (max-width: 629px) {
    .quick-view {
        width: 300px;
        padding: 16px 0px 0px;
    }

    .quick-view__link {
        width: 130px;
    }
}
@media (min-width: 630px) and (max-width: 767px) {
    .quick-view {
        width: 590px;
    }

    .quick-view__link {
        width: 406px;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .quick-view {
        width: 768px;
        padding: 8px 20px 0px;
    }

    .quick-view__link {
        width: 535px;
    }
}
</style>
