<template>
    <div class="news-section">
        <MainNews />
        <RelatedNews />
    </div>
</template>

<script>
import MainNews from "./MainNews.vue";
import RelatedNews from "./RelatedNews.vue";

export default {
    name: "NewsSection",
    props: {
        msg: String,
    },
    components: {
        MainNews,
        RelatedNews,
    },
};
</script>

<style scoped>
.news-section {
    padding: 16px 20px 0px;
    margin: 0px 0px 20px;
}

@media (min-width: 320px) and (max-width: 629px) {
    .news-section {
        align-self: center;

        padding: 8px 10px 0px;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .news-section {
        /* width: 866px; */
        padding: 0;
    }
}
</style>
