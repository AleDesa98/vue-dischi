<template>
    <form>
        <select v-model="filterGenre" @change="$emit('performeFilter', filterGenre)" name="genrename" id="genreid">
            <option value="">Seleziona un genere</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </form>
</template>

<script>
export default {
    name:"FilterGenre",
    data: function() {
        return {
            filterGenre: ''
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>