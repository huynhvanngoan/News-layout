<!-- MainNews.vue -->
<template>
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
</template>

<script>
import { defineComponent, ref } from "vue";
import { mainNewsCard, newsAds, relatedNews } from "@/data/mockData";
import CardNews from "@/components/CardNews.vue";

export default defineComponent({
    name: "MainNews",
    components: { CardNews },
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

@media (max-width: 629px) {
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
}

@media (min-width: 630px) and (max-width: 767px) {
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
}

@media (min-width: 768px) and (max-width: 1440px) {
    .main-news {
        width: 100%;
    }
}
</style>
