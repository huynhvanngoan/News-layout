<template>
    <div class="main-news">
        <MainNewsCard />
        <MainNewsAds />
    </div>
</template>

<script>
import MainNewsAds from "./MainNewsAds.vue";
import MainNewsCard from "./MainNewsCard.vue";

export default {
    name: "MainNews",
    props: {
        msg: String,
    },
    components: {
        MainNewsCard,
        MainNewsAds,
    },
};
</script>

<style scoped>
/* Main News */
.main-news {
    display: flex;
    flex-direction: row;
    align-items: center;
}

@media (min-width: 320px) and (max-width: 629px) {
    .main-news {
        justify-content: center;
        align-items: center;
        width: 316px;
    }
}
</style>
