<template>
    <section class="container">
        <Album :info="obj" v-for="(obj, index) in albumsFiltered" :key="index" />
    </section>
</template>

<script>
import axios from "axios";
import Album from "./Album.vue";

export default {
    name: "Albums",
    components: {
    Album,
    },
    props: ["optionSelected"],
    data() {
    return {
        albums: [],
    };
    },
    created() {
    axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
        this.albums = res.data.response;
        });
    },
    computed: {
    albumsFiltered() {
        return this.albums.filter((album) => {
            if (album.genre == this.optionSelected || this.optionSelected == "") {
                return true;
            }
            return false;
        });
    },
    },
};
</script>

<style lang="scss" scoped>
.container {
    margin-top: 50px;
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
}
</style>