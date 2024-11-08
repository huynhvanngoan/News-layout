<template>
    <div class="sidebar">
        <div class="sidebar__advertisement">
            <img src="../assets/Banne-biker-vn.webp" alt="" />
        </div>
        <div class="sidebar__community">
            <h3 class="sidebar__community-title">Cộng đồng</h3>
            <ul class="sidebar__community-list">
                <li class="sidebar__community-item">
                    <img
                        src="../assets/hp.webp"
                        alt="Community Item"
                        class="sidebar__community-image"
                    />
                    <span class="sidebar__community-label">HP</span>
                </li>
                <li class="sidebar__community-item">
                    <img
                        src="../assets/ttai.webp"
                        alt="Community Item"
                        class="sidebar__community-image"
                    />
                    <span class="sidebar__community-label">Tinh Tế AI</span>
                </li>
                <li class="sidebar__community-item">
                    <img
                        src="../assets/garmin.webp"
                        alt="Community Item"
                        class="sidebar__community-image"
                    />
                    <span class="sidebar__community-label"
                        >Garmin Việt Nam</span
                    >
                </li>
                <li class="sidebar__community-item">
                    <img
                        src="../assets/sw.webp"
                        alt="Community Item"
                        class="sidebar__community-image"
                    />
                    <span class="sidebar__community-label">HP</span>
                </li>
            </ul>
            <button href="#" class="sidebar__view-all">Xem tất cả (90)</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "SidebarView",
    props: {
        msg: String,
    },
};
</script>

<style scoped>
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
    .sidebar {
        width: 300px;

        padding: 16px 5px 0px 0px;
    }
    .sidebar__advertisement {
        display: none;
    }

    .sidebar__community-item {
        width: 125px;
        height: 100px;
    }
}

@media (min-width: 630px) and (max-width: 767px) {
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
    .sidebar {
        display: none;
    }
}
</style>
