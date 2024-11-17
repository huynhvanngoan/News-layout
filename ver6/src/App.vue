<template>
    <div class="main-container">
        <div class="wrapper">
            <div class="main-news">
                <CardNews
                    :imageSrc="mainNewsCard.imageSrc"
                    :title="mainNewsCard.title"
                    :source="mainNewsCard.source"
                    :url="mainNewsCard.url"
                    :showCommentIcon="true"
                    cardType="main"
                />

                <CardNews
                    :imageSrc="newsAds.imageSrc"
                    :title="newsAds.title"
                    :source="newsAds.source"
                    :description="newsAds.description"
                    :showCommentIcon="true"
                    cardType="ads"
                />

                <ul class="related-news">
                    <li v-for="news in relatedNews" :key="news.id">
                        <CardNews
                            :imageSrc="news.imageSrc"
                            :title="news.title"
                            :source="news.source"
                            :url="news.url"
                            :showCommentIcon="true"
                            cardType="related"
                        />
                    </li>
                </ul>
            </div>
            <div class="quick-view">
                <div class="quick-view__container">
                    <div class="quick-view__header">
                        <h3 class="quick-view__title">Xem nhanh</h3>
                        <a href="#" class="quick-view__view-all">Xem tất cả</a>
                    </div>
                    <div class="quick-view__list">
                        <QuickViewItem
                            v-for="item in quickViewList"
                            :key="item.id"
                            :item="item"
                        />
                    </div>
                </div>
            </div>
        </div>
        <div class="highlighted-news">
            <div class="featured-articles">
                <h2 class="featured-articles__title">Bài nổi bật</h2>
                <ul class="featured-articles__list">
                    <FeaturedItem
                        v-for="article in featuredArticles"
                        :key="article.rank"
                        :article="article"
                    />
                </ul>
            </div>
            <div class="sidebar">
                <div class="sidebar__advertisement">
                    <img
                        src="https://photo2.tinhte.vn/data/attachment-files/2024/07/8383266_Banne-biker-vn.jpg"
                        alt=""
                    />
                </div>
                <div class="sidebar__community">
                    <h3 class="sidebar__community-title">Cộng đồng</h3>
                    <ul class="sidebar__community-list">
                        <li
                            v-for="item in communityList"
                            :key="item.id"
                            class="sidebar__community-item"
                        >
                            <img
                                :src="item.imageSrc"
                                :alt="item.altText"
                                class="sidebar__community-image"
                            />
                            <span class="sidebar__community-label">{{
                                item.label
                            }}</span>
                        </li>
                    </ul>
                    <button href="#" class="sidebar__view-all">
                        Xem tất cả (90)
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CardNews from "./components/CardNews.vue";
import FeaturedItem from "./components/FeaturedItem.vue";
import QuickViewItem from "./components/QuickViewItem.vue";
import {
    newsAds,
    relatedNews,
    mainNewsCard,
    quickViewList,
    featuredArticles,
    communityList,
} from "./data/mockData";
export default {
    name: "App",
    components: {
        FeaturedItem,
        CardNews,
        QuickViewItem,
    },
    data() {
        return {
            newsAds,
            relatedNews,
            mainNewsCard,
            quickViewList,
            featuredArticles,
            communityList,
        };
    },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&display=swap");

:root {
    --color-primary: rgb(57, 134, 238);
    --color-secondary: #2d3748;
    --color-tertiary: #344054;
    --color-border: #1570ef;
    --color-background-light: #f1f2f4;
    --color-background-dark: #e5e6ed;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Lato", Arial, sans-serif;
}

ul {
    list-style: none;
}

hr {
    margin-right: 29%;
    margin-bottom: 20px;
    border: none;
    height: 2px;
    background-color: var(--color-background-dark);
}

.main-container {
    width: 100%;
    height: 100%;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.wrapper {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.main-news {
    width: 866px;
    padding: 16px 20px 0px;
    margin: 0px 20px 20px;
    display: grid;
    grid-template-areas:
        "main-card ads"
        "related related";
    grid-template-columns: 2fr 1fr;
    gap: 16px;
}

.related-news {
    grid-area: related;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 8px;
}

.related-news li:last-child {
    display: none;
}

.quick-view {
    width: 350px;
    display: flex;
    flex-direction: column;
    align-self: start;
    padding: 32px 20px 0px 0px;
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

.highlighted-news {
    display: flex;
    flex-direction: row;
}
.featured-articles {
    display: flex;
    flex-direction: column;
    padding: 16px 20px 0px;
}

.featured-articles__list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.sidebar {
    width: 350px;
    padding: 16px 20px 0px 0px;
    display: flex;
    flex-direction: column;
}

.sidebar__advertisement img {
    width: 100%;
    object-fit: contain;
    margin: 16px 0px;
}

.sidebar__community {
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 12px;
    border: 1px solid var(--color-background-dark);
    border-radius: 8px;
    margin: 0px 0px 16px;
}

.sidebar__community-title {
    padding-left: 4px;
    font-size: 18px;
    color: var(--color-secondary);
    margin: 0px 0px 16px;
    padding: 16px;
}

.sidebar__community-list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-items: center;
}

.sidebar__community-item {
    width: 152px;
    height: 117px;
    padding: 0px 4px 8px;
    display: flex;
    flex-direction: column;
    border-radius: 5px;
}

.sidebar__community-image {
    width: 100%;
    height: 81px;
    object-fit: cover;
    border-radius: 10px;
}

.sidebar__community-label {
    margin: 4px 0px 0px;
    font-size: 14px;
    color: var(--color-secondary);
}

.sidebar__view-all {
    height: 38px;
    padding: 7px 16px;
    border: none;
    outline: none;
    background: var(--color-background-dark);
    font-size: 12px;
    line-height: 24px;
    color: var(--color-secondary);
    border-radius: 4px;
    font-weight: 700;
}

@media (min-width: 320px) and (max-width: 629px) {
    .main-container {
        padding: 0;
    }

    .wrapper {
        flex-direction: column;
    }

    .main-news {
        width: 100%;
        grid-template-areas:
            "main-card"
            "related";
        grid-template-columns: 1fr;
    }
    .related-news li:last-child {
        display: block;
    }

    .quick-view {
        width: 100%;
        padding: 16px 16px 0px;
    }

    .highlighted-news {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .featured-articles {
        margin-top: 16px;
        padding: 8px 10px 0px;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
    }

    .sidebar {
        display: none;
        width: 100%;

        padding: 16px 5px 0px 0px;
    }
    .sidebar__advertisement {
        display: none;
    }

    .sidebar__community-item {
        width: calc(100% / 2);
        height: 100px;
    }

    .sidebar__community-image {
        width: 100%;
        height: 200px;
        object-fit: cover;
        border-radius: 10px;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .main-container {
        padding: 8px 20px 0px;
    }

    .wrapper {
        flex-direction: column;
    }

    .main-news {
        width: 100%;
        grid-template-areas:
            "main-card"
            "related";
        grid-template-columns: 1fr;
    }
    .related-news li {
        height: auto;
    }
    .related-news li:last-child {
        display: block;
    }

    .quick-view {
        width: 100%;
    }

    .highlighted-news {
        margin-top: 16px;
        display: flex;
        flex-direction: column;
        padding: 8px 15px 0px;
    }

    .featured-articles {
        padding: 0;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }
    .sidebar {
        width: 590px;
        align-self: center;
        padding: 0;
    }

    .sidebar__advertisement {
        display: none;
    }

    .sidebar__community-title {
        padding: 0;
    }

    .sidebar__community-item {
        width: 282px;
        height: 190.13px;
    }

    .sidebar__community-image {
        width: 100%;
        height: 200px;
        object-fit: cover;
        border-radius: 10px;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .wrapper {
        flex-direction: column;
    }

    .main-news {
        width: 100%;
    }

    .quick-view {
        width: 100%;
        padding: 8px 20px 0px;
    }

    .highlighted-news {
        display: flex;
        flex-direction: column;
    }

    .featured-articles__list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }

    .sidebar {
        display: none;
    }
}

@media (min-width: 1024px) and (max-width: 1440px) {
    .main-news {
        width: 100%;
    }

    .highlighted-news {
        width: 100%;
    }

    .featured-articles {
        width: 80%;
    }
}
</style>
