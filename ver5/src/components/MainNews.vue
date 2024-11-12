
<template>
    <div class="main-news">
        <div class="main-news__card">
            <img :src="mainNewsCard.imageSrc" alt="" class="main-news__image" />
            <a :href="mainNewsCard.url" class="main-news__title">
                {{ mainNewsCard.title }}
            </a>
            <div class="source-comment">
                <span class="main-news__source">{{ mainNewsCard.source }}</span>
                <img src="../assets/comment.svg" alt="" class="news-comment" />
            </div>
        </div>
        <div class="main-news__ads">
            <div class="news-ads__container">
                <div class="ads__image-container">
                    <img :src="newsAds.imageSrc" alt="" class="ads__image" />
                </div>
                <div class="ads__content">
                    <a href="#" class="ads__title">{{ newsAds.title }}</a>
                    <div class="source-comment">
                        <span class="ads__source">{{ newsAds.source }}</span>
                        <span class="news-comment">
                            <img
                                src="../assets/comment.svg"
                                alt="Comment"
                                class="news-comment"
                            />
                        </span>
                    </div>
                    <p class="ads__description">{{ newsAds.description }}</p>
                </div>
            </div>
        </div>
        <ul class="related-news">
            <li
                v-for="news in relatedNews"
                :key="news.id"
                class="related-news__card"
            >
                <img :src="news.imageSrc" alt="" class="related-news__image" />
                <a :href="news.url" class="related-news__title">{{
                    news.title
                }}</a>
                <div class="source-comment">
                    <span class="related-news__source">{{ news.source }}</span>
                    <span class="news-comment">
                        <img
                            src="../assets/comment.svg"
                            alt="Comment"
                            class="news-comment"
                        />
                    </span>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
import { defineComponent, ref } from "vue";
import { mainNewsCard, newsAds, relatedNews } from "@/data/mockData";

export default defineComponent({
    name: "MainNews",
    setup() {
        const cardData = ref(mainNewsCard);
        const newsAdsData = ref(newsAds);

        return {
            mainNewsCard: cardData,
            newsAds: newsAdsData,
            relatedNews,
        };
    },
});
</script>

<style scoped>
/* Main News */
.main-news {
    width: 866px;
    /* padding: 16px 20px 0px; */
    margin: 0px 20px 20px;
    display: grid;
    grid-template-areas:
        "main-card ads"
        "related related";
    grid-template-columns: 2fr 1fr;
    grid-template-rows: auto auto;
    gap: 16px;
}

.main-news__card {
    grid-area: main-card;
    /* height: 471.02px; */
    display: flex;
    flex-direction: column;
    gap: 10px;
    /* padding: 0px 8px; */
}

.main-news__image {
    width: 100%;
    /* height: 337.55px; */
    border-radius: 8px;
    object-fit: cover;
}

.main-news__title {
    font-size: 22px;
    line-height: 30px;
    font-weight: 700;
    color: var(--color-secondary);
    text-decoration: none;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}

a:hover {
    color: var(--color-primary);
}

.main-news__source {
    color: var(--color-secondary);
    text-decoration: none;
    font-size: 13px;
    font-weight: 400;
    line-height: 18px;
}

.main-news__ads {
    grid-area: ads;
    /* padding: 0px 8px; */
    /* height: 471.02px; */
    transition: all 0.2s linear;
}

.news-ads__container {
    border-radius: 8px 8px 0 0;
    display: flex;
    flex-direction: column;
    gap: 12px;
    background: linear-gradient(
        180deg,
        var(--color-background-dark) 41.65%,
        var(--color-background-light) 80.57%,
        #ffffff 96.86%
    );
}

.ads__image-container {
    width: 100%;
    height: 185px;
}

.ads__image {
    width: 100%;
    height: 100%;
    border-radius: 8px 8px 0 0;
    object-fit: cover;
}

.ads__content {
    width: 100%;
    /* height: 275.02px; */
    overflow: hidden;
    display: flex;
    flex-direction: column;
    padding: 0px 16px 12px;
}

.ads__title {
    color: var(--color-secondary);
    font-size: 16px;
    line-height: 20px;
    font-weight: 700;
    margin: 0px 0px 8px;
    text-decoration: none;
}

.ads__source {
    font-size: 13px;
    color: var(--color-secondary);
    margin: 0px 0px 3px;
}

.ads__description {
    color: var(--color-tertiary);
    font-size: 16px;
    line-height: 24px;
    font-weight: 400;
    text-wrap: wrap;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 7;
    -webkit-box-orient: vertical;
}

.related-news {
    grid-area: related;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 8px;
    margin: 0px 0px 20px;
    padding: 0px 0px 5px;
}

.related-news__card {
    display: flex;
    flex-direction: column;
    /* height: 295px; */
    padding: 0px 8px;
}

.related-news .related-news__card:last-child {
    display: none;
}

.related-news__image {
    width: 100%;
    height: 163.81px;
    border-radius: 4px;
    object-fit: cover;
}

.related-news__title {
    font-size: 16px;
    line-height: 22px;
    font-weight: bold;
    color: var(--color-secondary);
    text-decoration: none;
    margin: 12px 0px 8px;
}

.related-news__source {
    font-size: 13px;
    line-height: 18px;
    font-weight: 400;
    color: var(--color-secondary);
}

@media (max-width: 629px) {
    .main-news {
        width: 100%;
        grid-template-areas:
            "main-card"
            "related";
        grid-template-columns: 1fr;
    }

    .main-news__ads {
        display: none;
    }
    .related-news .related-news__card:last-child {
        display: block;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .main-news {
        width: 100%;
        grid-template-areas:
            "main-card"
            "related";
        grid-template-columns: 1fr;
    }

    .main-news__ads {
        display: none;
    }

    .related-news .related-news__card:last-child {
        display: block;
    }

    .related-news__card {
        height: auto;
    }
}

@media (min-width: 768px) and (max-width: 1440px) {
    .main-news {
        width: 100%;
    }
}
</style>
