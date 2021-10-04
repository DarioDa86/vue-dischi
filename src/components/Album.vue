<template>
    <div class="album">
        <div class="image-album">
            <img :src="info.poster" :alt="info.title">
        </div>
        <h4 class="name-album">{{info.title}}</h4>
        <div class="name-author">{{info.author}}</div>
        <div class="year-album">{{info.year}}</div>
    </div>
</template>

<script>
export default {
    name: "Album", 
    props: {
        info: Object
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

.album {
    width: calc(20% - 40px);
    margin: 10px 20px;
    background-color: $BgHeader;
    text-align: center;
    padding: 10px;
    
    .image-album {
        width: 0 auto;
        padding: 10px;
        
        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .name-album {
        color: #fff;
        text-transform: uppercase;
        margin-bottom: 10px;
        font-size: 20px;
    }

    .name-author, .year-album {

        color: gray
    }

    .year-album {

        margin-bottom: 10px;
    }
}

</style>