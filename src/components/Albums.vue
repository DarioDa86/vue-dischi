<template>
    <section class="albums container" >
        <div class="albums" v-for="(obj, index) in albums" :key="index">
            <Album :info="obj"/>
        </div>
        
    </section>
</template>

<script>
import axios from 'axios';
import Album from '.src/components/Album.vue'; 

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
                this.albums = res.data;
            });
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