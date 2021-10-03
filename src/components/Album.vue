<template>
    <div class="album">
        <div class="image-album">
            <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="foto casuale">
        </div>
        <h4 class="name-album">New Jersey</h4>
        <div class="name-author">Bon Jovi</div>
        <div class="year-album">1988</div>
    </div>
    
    
</template>

<script>
export default {
    name: "Album"

}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

.album {

    width: calc(20% - 40px);
    border: 1px solid #fff;

    margin: 10px 20px;
    background-color: $BgHeader;
    text-align: center;
    
    .image-album {
        border: 1px solid #fff;
        

        img {

            width: 100%;
            object-fit: cover;
        }
    }

    .name-album {
        color: #fff;
        text-transform: uppercase;
        margin-bottom: 10px;
    }
}

</style>