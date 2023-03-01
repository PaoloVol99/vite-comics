<script>
export default {
    data() {
        return {
            navbarItems: [
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop'
            ],
            activeIndex: 1
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="col">
                <img src="/img/dc-logo.png" alt="">
            </div>
            <div class="col">
                <nav>
                    <ul class="navbar">
                        <li v-for="(element, index) in navbarItems" :class="index === activeIndex ? 'active' : ''" class="nav-item"> {{ element }}</li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>

@use '../style/partials/variables.scss' as*;
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
        max-width: 70px;
    }

    .navbar {
        display: flex;
        gap: 20px;

        .nav-item {
            line-height: 90px;
            text-transform: uppercase;
            font-size: 12px;
            font-weight: 600;

            &.active,
            &:hover {
                color: $dc-blue;
                border-bottom: 4px solid $dc-blue;
                cursor: pointer;
            }
        }
    }

}

</style>