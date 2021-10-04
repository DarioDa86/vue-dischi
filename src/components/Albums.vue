<template>
    <section class="container" >
        <div class="albums" v-for="(obj, index) in albums" :key="index">
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
            <Album :info="obj"/>
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import Album from './Album.vue'; 

export default {
    name: "Albums",
    components: {
        Album
    },
    data() {
        return {
            albums: []
        }
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) => {
                this.albums = res.data.response;
            });
    }
}
</script>

<style lang="scss" scoped>

.albums {

        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
        margin-top: 50px;
}

</style>