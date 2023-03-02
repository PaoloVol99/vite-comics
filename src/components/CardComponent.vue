<script>
export default {
    props: {
        img: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        }
    }

}
</script>

<template>
    <div class="card">
        <img .src="img" alt="">
        <h3>{{ title }}</h3>
    </div>
</template>


<style lang="scss" scoped>
.card {
    img {
        aspect-ratio: 1;
        object-fit: cover;
    }

    h3 {
        font-weight: 300;
        font-size: 16px;
        margin-top: 10px;
    }
}

</style>