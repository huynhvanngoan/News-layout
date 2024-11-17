<template>
    <li class="featured-articles__item">
        <div class="featured-articles__info">
            <p class="featured-articles__rank">#{{ article.rank }}</p>
            <div class="featured-articles__details">
                <a :href="article.url" class="featured-articles__title">
                    {{ article.title }}
                </a>
                <span class="featured-articles__source">{{
                    article.source
                }}</span>
            </div>
        </div>
    </li>
</template>

<script>
export default {
    name: "FeaturedItem",
    props: {
        article: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style scoped>
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

@media (min-width: 630px) and (max-width: 767px) {

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
    .sidebar {
        display: none;
    }
}

@media (min-width: 1024px) and (max-width: 1440px) {
    .featured-articles__item {
        width: 100%;
    }
}
</style>
