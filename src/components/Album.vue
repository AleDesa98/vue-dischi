<template>
    <section>
        <img :src="item.poster" alt="">
        <h3>{{ item.title }}</h3>
        <p>{{ item.author }}</p>
        <p>{{ item.year }}</p>
    </section>
</template>

<script>
export default {
    name: "Album",
    props: [ "item" ]
}
</script>

<style lang="scss" scoped>
    section {
        background-color: #2D3B46;
        padding: 20px;
        height: 100%;
        cursor: pointer;
        img {
            width: 100%;
        }
        h3 {
            color: white;
            margin: 20px 0;
            font-size: 26px;
            text-align: center;
        }
        p {
            color: #607078;
            text-align: center;
            margin: 0;
            font-size: 20px;
        }
    }
</style>