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
        <div class="container">
            <div class="row">
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
    padding: 50px 0;
    
    .row {
        color: white;
        display: flex;
        flex-wrap: wrap;
        margin: 0 -12px;
        row-gap: 40px;
        .col {
            width: calc(100% / 6);
            padding: 0 12px;
        }
    }
}


</style>