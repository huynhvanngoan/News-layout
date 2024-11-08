<template>
    <div class="main-news__ads">
        <div class="news-ads__container">
            <div class="ads__image-container">
                <img src="../assets/ads1.webp" alt="" class="ads__image" />
            </div>
            <div class="ads__content">
                <a class="ads__title">
                    Đặt luôn Mac mini M4 16GB không do dự, 15 triệu là mức giá
                    quá tốt
                </a>
                <div class="source-comment">
                    <span class="ads__source">Lê Huyền Vân</span>
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
                <p class="ads__description">
                    Apple đưa ra mức giá khởi điểm quá tốt cho Mac mini M4 cấu
                    hình cơ bản 16GB RAM mới ra mắt, 15 triệu đồng. Mức chi phí
                    này có thể khiến người dùng đồ Apple ít phải đắn đo, đồng
                    thời nó cũng hợp túi tiền cho HSSV với 12,5 triệu.
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "MainNewsAds",
    props: {
        msg: String,
    },
};
</script>

<style scoped>
/* Ads Section */
.main-news__ads {
    padding: 0px 8px;
    width: 280.66px;
    height: 471.02px;
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
    /* width: 100%; */
    height: 275.02px;
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

@media (min-width: 320px) and (max-width: 629px) {
    .main-news__ads {
        display: none;
    }
}
@media (min-width: 630px) and (max-width: 767px) {
    .main-news__ads {
        display: none;
    }
}

@media (min-width: 768px) and (max-width: 1023px) {
    .main-news__ads {
        height: 424.59px;
        width: 248px;
    }

    .ads__image-container {
        height: 144px;
    }
    .ads__description {
        -webkit-line-clamp: 7;
    }
}

@media (min-width: 1024px) and (max-width: 1440px) {
    .main-news__ads {
        height: 425.2px;
        width: 216.67px;
    }

    .ads__image-container {
        height: 124.2px;
    }
    .ads__description {
        -webkit-line-clamp: 7;
    }
}
</style>
