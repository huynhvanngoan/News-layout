<template>
    <div class="highlighted-news">
        <div class="featured-articles">
            <h2 class="featured-articles__title">Bài nổi bật</h2>
            <ul class="featured-articles__list">
                <li
                    v-for="article in featuredArticles"
                    :key="article.rank"
                    class="featured-articles__item"
                >
                    <div class="featured-articles__info">
                        <p class="featured-articles__rank">
                            #{{ article.rank }}
                        </p>
                        <div class="featured-articles__details">
                            <a
                                :href="article.url"
                                class="featured-articles__title"
                            >
                                {{ article.title }}
                            </a>
                            <span class="featured-articles__source">{{
                                article.source
                            }}</span>
                        </div>
                    </div>
                </li>
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
</template>

<script>
import { featuredArticles, communityList } from "@/data/mockData";

export default {
    name: "HighlightNews",
    props: {
        msg: String,
    },
    data() {
        return {
            featuredArticles,
            communityList,
        };
    },
};
</script>

<style scoped>
.highlighted-news {
    display: flex;
    flex-direction: row;
}
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
    .featured-articles__item {
        width: 100%;
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
        width: calc(100%/2);
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
    .highlighted-news {
        /* width: 630px; */
        margin-top: 16px;
        display: flex;
        flex-direction: column;
        padding: 8px 15px 0px;
    }

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
    .highlighted-news {
        display: flex;
        flex-direction: column;
    }
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
    .highlighted-news {
        width: 100%;
    }
    .featured-articles {
        width: 80%;
    }
    .featured-articles__item {
        width: 100%;
    }
}
</style>
