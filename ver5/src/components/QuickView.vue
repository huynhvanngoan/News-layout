<template>
    <div class="quick-view">
        <div class="quick-view__container">
            <div class="quick-view__header">
                <h3 class="quick-view__title">Xem nhanh</h3>
                <a href="#" class="quick-view__view-all">Xem tất cả</a>
            </div>
            <div class="quick-view__list">
                <div
                    v-for="item in quickViewList"
                    :key="item.id"
                    class="quick-view__item"
                >
                    <div class="quick-view__timeline-dot"></div>
                    <div class="quick-view__content">
                        <a :href="item.url" class="quick-view__link">
                            {{ item.title }}
                        </a>
                        <img
                            :src="item.imageSrc"
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
import { quickViewList } from "../data/mockData";
export default {
    name: "QuickView",
    props: {
        msg: String,
    },
    data() {
        return {
            quickViewList,
        };
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
    justify-content: space-between;
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
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.quick-view__link {
    width: 75%;
    padding-right: 12px;
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
        width: 100%;
        padding: 16px 16px 0px;
    }

    .quick-view__image {
        width: 120px;
        height: 60px;
    }
    
}
@media (min-width: 630px) and (max-width: 767px) {
    .quick-view {
        width: 100%;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .quick-view {
        width: 100%;
        padding: 8px 20px 0px;
    }
}
</style>
