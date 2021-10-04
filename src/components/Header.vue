<template>
    <header>
        <div class="logo-spotify">
            <img src="../assets/images/spotify-logo.png" alt="logo spotify">
        </div>
        <GenreSelect/>
    </header>
</template>

<script>
import GenreSelect from './GenreSelect.vue'; 

export default {
    components: {
        GenreSelect
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
            height: 80px;
            margin: 10px;
        }
    }
}

</style>