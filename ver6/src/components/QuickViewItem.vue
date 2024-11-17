<template>
    <div class="quick-view__item">
        <div class="quick-view__timeline-dot"></div>
        <div class="quick-view__content">
            <a :href="item.url" class="quick-view__link">
                {{ item.title }}
            </a>
            <img
                :src="item.imageSrc"
                alt="News Image"
                class="quick-view__image"
            />
        </div>
    </div>
</template>

<script>
export default {
    name: "QuickViewItem",
    props: {
        item: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style scoped>
.quick-view__item {
    width: 100%;
    display: flex;
    gap: 10px;
    align-items: center;
    justify-content: space-between;
    margin: 0px 0px 16px;
}

.quick-view__timeline-dot {
    margin-bottom: 40px;
    position: absolute;
    left: -5px;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: var(--color-primary);
}

.quick-view__content {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.quick-view__link {
    width: 75%;
    padding-right: 12px;
    font-size: 14px;
    line-height: 20px;
    font-weight: 700;
    color: var(--color-secondary);
    font-weight: bold;
    text-decoration: none;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}

.quick-view__link:hover {
    color: var(--color-primary);
}

.quick-view__image {
    width: 120px;
    height: 60px;
    border-radius: 5px;
    object-fit: cover;
}

@media (min-width: 320px) and (max-width: 629px) {
    .quick-view__image {
        width: 120px;
        height: 60px;
    }
}
</style>
