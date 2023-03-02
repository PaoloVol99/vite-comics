<script>
import MainItems from '../dc-comics.json'
import CardComponent from './CardComponent.vue'

export default {
    components: {
        CardComponent
    },
    data() {
        return {
            mainItems: MainItems
        }
    }

}
</script>

<template>
    <main>
        <img class="jumbotron" src="/img/jumbotron.jpg" alt="">
        <div class="container">
            <div class="row">
                <span>current series</span>
                <div v-for="(el,i) in mainItems" :key="i" class="col">
                    <CardComponent :title="el.series" :img="el.thumb" />
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as*;

main {
    background-color: $dc-dark-grey;
    padding: 0 0 50px;
    .jumbotron {
        height: 310px;
        object-fit: cover;
        width: 100%;
        object-position: top;
        display: block;
    }
    
    .row {
        color: white;
        display: flex;
        flex-wrap: wrap;
        margin: 0 -12px;
        row-gap: 40px;
        padding-top: 40px;
        position: relative;

        span {
            position: absolute;
            top: 0;
            left: 0;
            transform: translate(0, -50%);
            background-color: $dc-blue;
            padding: 0 20px;
            line-height: 50px;
            text-transform: uppercase;
            font-weight: 600;
            font-size: 18px;
        }
        .col {
            width: calc(100% / 6);
            padding: 0 12px;
            text-transform: uppercase;
        }
    }
}


</style>