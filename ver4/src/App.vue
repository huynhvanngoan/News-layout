<template>
    <div class="main-container">
        <div class="wrapper">
            <NewsSection />
            <QuickView />
        </div>
        <HighlightNews />
    </div>
</template>

<script>
import HighlightNews from "./components/HighlightNews.vue";
import NewsSection from "./components/NewsSection.vue";
import QuickView from "./components/QuickView.vue";

export default {
    name: "App",
    components: {
        NewsSection,
        QuickView,
        HighlightNews,
    },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&display=swap");

/* Color Variables */
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

/* Body Styles */
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
    width: 840px;
    margin-right: 19%;
    margin-bottom: 20px;
    border: none; /* Xóa viền mặc định */
    height: 2px; /* Đặt chiều cao cho đường */
    background-color: var(--color-background-dark);
}
/* Main Container */
.main-container {
    width: 100%;
    height: 100%;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* gap: 60px; */
}

/* Wrapper */
.wrapper {
    display: flex;
    flex-direction: row;
    /* align-items: start; */
    justify-content: center;
    align-items: center;
    /* gap: 18px; */
}

.source-comment {
    display: flex;
    /* justify-content: center; */
    align-items: center;
}

.news-comment {
    padding-top: 0.7px;
    margin-left: 8px;
}
@media (min-width: 320px) and (max-width: 629px) {
    .main-container {
        padding: 0;
    }
    .wrapper {
        flex-direction: column;
    }
}
@media (min-width: 630px) and (max-width: 767px) {
    .main-container {
        width: 630px;
        padding: 8px 20px 0px;
    }
    .wrapper {
        flex-direction: column;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .wrapper {
        flex-direction: column;
    }
}
</style>
