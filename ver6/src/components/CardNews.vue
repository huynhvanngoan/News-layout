<template>
    <div :class="`card ${cardTypeClass}`">
        <img :src="imageSrc" :alt="title" class="card-image" v-if="imageSrc" />
        <div class="card-content">
            <a :href="url" class="card-title">{{ title }}</a>
            <div class="card__source-comment" v-if="source || showCommentIcon">
                <span class="card__source" v-if="source">{{ source }}</span>
                <img
                    src="../assets/comment.svg"
                    alt="Comment"
                    class="card__comment-icon"
                    v-if="showCommentIcon"
                />
            </div>
            <p class="card-description" v-if="description">
                {{ description }}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardNews",
    props: {
        imageSrc: String,
        title: String,
        source: String,
        description: String,
        url: String,
        showCommentIcon: {
            type: Boolean,
            default: false,
        },
        cardType: {
            type: String,
            default: "default",
        },
    },
    computed: {
        cardTypeClass() {
            return `card-${this.cardType}`;
        },
    },
};
</script>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.card-ads {
    border-radius: 8px 8px 0 0;
    gap: 12px;
    background: linear-gradient(
        180deg,
        var(--color-background-dark) 41.65%,
        var(--color-background-light) 80.57%,
        #ffffff 96.86%
    );
}

.card-ads .card-content {
    width: 100%;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    padding: 0px 16px 12px;
}

.card-ads .card-image {
    height: 164px;
}

.card-image {
    width: 100%;
    border-radius: 8px;
    object-fit: cover;
}

.card-title {
    margin-bottom: 8px;
    font-size: 16px;
    line-height: 22px;
    font-weight: bold;
    color: var(--color-secondary);
    text-decoration: none;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    cursor: pointer;
}

.card-title:hover {
    color: var(--color-primary);
}
.card__source-comment {
    display: flex;
    align-items: center;
    gap: 4px;
}

.card__source {
    font-size: 13px;
    color: var(--color-secondary);
}

.card__comment-icon {
    width: 16px;
    height: 16px;
}

.card-description {
    font-size: 14px;
    line-height: 20px;
    color: var(--color-tertiary);
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 7;
    -webkit-box-orient: vertical;
}

.card-main .card-title {
    font-size: 22px;
    font-weight: 700;
}

.card-ads .card-description {
    -webkit-line-clamp: 7;
}

.card-related .card-image {
    height: 164px;
}

@media (max-width: 629px) {
    .card-ads {
        display: none;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
    .card-ads {
        display: none;
    }
}
</style>
