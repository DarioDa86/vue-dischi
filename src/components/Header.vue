<template>
    <header>
        <div class="logo-spotify">
            <img src="../assets/images/spotify-logo.png" alt="logo spotify">
        </div>
        <select name="" id="" v-model="optionValue" @change="$emit('optionChanged', optionValue)">
            <option value="">All</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Rock">Rock</option>
            <option value="Metal">Metal</option>
        </select>
    </header>
</template>

<script>

export default {
    name: "Header",
    data() {
        return {
            optionValue: ""
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

header {
    background-color: $BgHeader;
    display: flex;
    justify-content: space-between;

    .logo-spotify{

        img{
            height: 60px;
            margin: 10px;
        }
    }

    select {
        margin: 30px;
    }
}

</style>