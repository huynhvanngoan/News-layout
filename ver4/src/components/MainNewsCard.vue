<template>
    <div class="main-news__card">
        <img src="../assets/mainNews.webp" alt="" class="main-news__image" />
        <a href="/" class="main-news__title"
            >Bạn "phải" lật đít Mac mini lên để bấm nút nguồn...</a
        >
        <div class="source-comment">
            <span class="main-news__source">cuhiep</span>
            <span class="news-comment"
                ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="21"
                    height="21"
                    viewBox="0 0 25 21"
                >
                    <g fill="none" fill-rule="evenodd">
                        <text
                            fill="#313131"
                            font-family="Lato-Regular, Lato"
                            font-size="12.744"
                            letter-spacing=".679"
                            transform="translate(-211 3)"
                        >
                            <tspan x="100" y="13">57 minutes ago</tspan>
                            <tspan
                                x="242.728"
                                y="13"
                                font-family="Lato-Bold, Lato"
                                font-weight="bold"
                            >
                                678
                            </tspan>
                            <tspan x="266.938" y="13"></tspan>
                        </text>
                        <g fill-rule="nonzero">
                            <path
                                fill="#44d7b6"
                                d="M19.873.024H5.127A5.133 5.133 0 0 0 0 5.151v7.919a5.046 5.046 0 0 0 3.627 4.85l2.476 2.476a.735.735 0 0 0 1.036 0l2.272-2.272h10.462c2.827 0 5.127-2.3 5.127-5.127V5.151C25 2.324 22.7.024 19.873.024z"
                            ></path>
                            <path
                                fill="#F2F0FF"
                                d="M7.85 8.512h9.3a.733.733 0 1 0 0-1.465h-9.3a.733.733 0 1 0 0 1.465zm0 2.589h9.3a.733.733 0 1 0 0-1.465h-9.3a.733.733 0 1 0 0 1.465z"
                            ></path>
                        </g>
                    </g>
                </svg>
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name: "MainNewsCard",
    props: {
        msg: String,
    },
};
</script>

<style scoped>
.main-news__card {
    width: 561.33px;
    height: 471.02px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 0px 8px;
}

.main-news__image {
    width: 100%;
    height: 337.55px;
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

@media (min-width: 320px) and (max-width: 629px) {
    .main-news__card {
        width: 316px;
        height: 312px;
    }

    .main-news__image {
        height: 186.59px;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .main-news__card {
        width: 606px;
        height: 461px;
    }

    .main-news__image {
        height: 365px;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .main-news__card {
        width: 496px;
        height: 424.59px;
    }

    .main-news__image {
        height: 297.11px;
    }
}
@media (min-width: 1024px) and (max-width: 1440px) {
    .main-news__card {
        width: 433.33px;
        height: 425.2px;
    }

    .main-news__image {
        height: 258px;
    }
}
</style>
