<script>
export default {

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
                        <li class="nav-item">Characters</li>
                        <li class="nav-item active">Comics</li>
                        <li class="nav-item">Movies</li>
                        <li class="nav-item">Tv</li>
                        <li class="nav-item">Games</li>
                        <li class="nav-item">Collectibles</li>
                        <li class="nav-item">Videos</li>
                        <li class="nav-item">Fans</li>
                        <li class="nav-item">News</li>
                        <li class="nav-item">Shop</li>
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