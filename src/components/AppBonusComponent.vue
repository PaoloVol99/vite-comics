<script>
export default {

}
</script>

<template>
    <div class="component-wrapper">
        <div class="container">
            <div class="icons-wrapper">
                <ul>
                    <li>
                        <img src="/img/buy-comics-digital-comics.png" alt="">
                        <span>digital comics</span>
                    </li>
                    <li>
                        <img src="/img/buy-comics-merchandise.png" alt="">    
                        <span>dc merchandise</span>
                    </li>
                    <li>
                        <img src="/img/buy-comics-subscriptions.png" alt="">
                        <span>subsctiption</span>
                    </li>
                    <li>
                        <img src="/img/buy-comics-shop-locator.png" alt="">
                        <span>comic shop locator</span>
                    </li>
                    <li>
                        <img class="power-visa" src="/img/buy-dc-power-visa.svg" alt="">
                        <span>dc power visa</span>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as*;

.component-wrapper {
    background-color: $dc-blue;

    .icons-wrapper {
        padding: 40px 0;
        ul{
            display: flex;
            align-items: center;
            gap: 50px;
            justify-content: center;

            li {
                display: flex;
                align-items: center;
                color: white;
                text-transform: uppercase;
                gap: 10px;
                font-size: 12px;

                img {
                    height: 50px;
    
                    
                }
                .power-visa {
                    height: 30px;
                }
            }    
        }
    }
    
}

</style>