<template>
    <div class="featured-articles">
        <h2 class="featured-articles__title">Bài nổi bật</h2>
        <ul class="featured-articles__list">
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#1</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Apple ra mắt Mac Mini mới: Nhỏ hơn, trang bị chip
                            M4 Pro, giá chỉ từ 14.9 triệu</a
                        >
                        <span class="featured-articles__source">Anh Tú.</span>
                    </div>
                </div>
            </li>
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#2</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Đặt luôn Mac mini M4 16GB không do dự, 15 triệu là
                            mức giá quá tốt</a
                        >
                        <span class="featured-articles__source"
                            >Lê Huyền Vân</span
                        >
                    </div>
                </div>
            </li>
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#3</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Xiaomi 15 Pro ra mắt: Snapdragon 8 Elite, Xiaomi
                            HyperOS 2, pin 6.100 mAh, giá từ 18.8 triệu</a
                        >
                        <span class="featured-articles__source"
                            >Cáo - Foxtek</span
                        >
                    </div>
                </div>
            </li>
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#4</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Hai vợ chồng tốn 15 năm đi kiện Google, kết quả
                            Google bị phạt hơn 3 tỷ USD</a
                        >
                        <span class="featured-articles__source">P.W</span>
                    </div>
                </div>
            </li>
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#5</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Hiểu được công suất máy hút ẩm để tính toán cho hợp
                            nhu cầu</a
                        >
                        <span class="featured-articles__source"
                            >Ngon Bổ Xẻ</span
                        >
                    </div>
                </div>
            </li>
            <li class="featured-articles__item">
                <div class="featured-articles__info">
                    <p class="featured-articles__rank">#6</p>
                    <div class="featured-articles__details">
                        <a href="#" class="featured-articles__title"
                            >Bóc Phốt FPT</a
                        >
                        <span class="featured-articles__source"
                            >Habe0212021</span
                        >
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "FeaturedArticles",
    props: {
        msg: String,
    },
};
</script>

<style scoped>
.featured-articles {
    /* width: 866px; */
    display: flex;
    flex-direction: column;
    padding: 16px 20px 0px;
}

.featured-articles__list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.featured-articles__item {
    padding: 16px 12px 0px;
    width: 421px;
    height: 87px;
}

.featured-articles__info {
    display: flex;
    flex-direction: row;
}

.featured-articles__rank {
    text-align: start;
    width: 70px;
    line-height: 42px;
    font-size: 42px;
    font-weight: 800;
    color: rgb(152, 162, 179);
}

.featured-articles__details {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.featured-articles__title {
    width: 100%;
    color: var(--color-secondary);
    font-size: 18px;
    text-decoration: none;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}

.featured-articles__source {
    color: var(--color-secondary);
    font-size: 13px;
    line-height: 18px;
    font-weight: 400;
}

@media (min-width: 320px) and (max-width: 629px) {
    .featured-articles {
        margin-top: 16px;
        padding: 8px 10px 0px;
    }
    .featured-articles__item {
        width: 300px;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .featured-articles {
        padding: 0;
    }

    .featured-articles__item {
        width: 307px;
        height: 131.56px;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .featured-articles__item {
        width: 376px;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 1024px) and (max-width: 1440px) {
    .featured-articles__item {
        width: 325px;
    }
}
</style>
