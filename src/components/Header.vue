<template>
    <header>
        <div class="logo-spotify">
            <img src="../assets/images/spotify-logo.png" alt="logo spotify">
        </div>
    </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

header {
    background-color: $BgHeader;

    .logo-spotify{

        img{
            height: 80px;
            margin: 10px;
        }
    }
}

</style>