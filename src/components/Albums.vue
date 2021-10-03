<template>
    <section class="albums container">
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        
    </section>
</template>

<script>
import Album from './Album.vue'; 

export default {
    name: "Albums",
    components: {
        Album
    }

}
</script>

<style lang="scss" scoped>

.albums {
    display: flex;
    flex-wrap: wrap;
    margin-top: 50px;
}

</style>