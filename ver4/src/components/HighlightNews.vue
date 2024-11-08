<template>
    <div class="highlighted-news">
        <FeaturedArticles />
        <SidebarView />
    </div>
</template>

<script>
import FeaturedArticles from "./FeaturedArticles.vue";
import SidebarView from "./Sidebar.vue";

export default {
    name: "HighlightNews",
    props: {
        msg: String,
    },
    components: {
        FeaturedArticles,
        SidebarView,
    },
};
</script>

<style scoped>
.highlighted-news {
    display: flex;
    flex-direction: row;
}
@media (min-width: 320px) and (max-width: 629px) {
    .highlighted-news {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .highlighted-news {
        /* width: 630px; */
        margin-top: 16px;
        display: flex;
        flex-direction: column;
        padding: 8px 15px 0px;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .highlighted-news {
        display: flex;
        flex-direction: column;
    }
}
</style>
