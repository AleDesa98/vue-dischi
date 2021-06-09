<template>
    <header>
        <a href="">
            <img src="../assets/img/spotify.png" alt="">
        </a>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>
    header {
        display: flex;
        align-items: center;
        background-color: #2D3B46;
        height: 70px;
        a {
            margin-left: 20px;
            img {
                height: 50px;
            }
        }
    }
</style>