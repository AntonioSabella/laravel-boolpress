<template>


    <div class="landscape p-5 bg-dark text-white">
        <div class="container text-center">
            <h1 class="display-3">
                Boolpress - My Blog
            </h1>
            <div class="work rounded d-flex justify-content-center py-3">
                <div class="logo">
                    <img width="200"  class="img-fluid" src="https://upload.wikimedia.org/wikipedia/commons/9/93/Wordpress_Blue_logo.png" alt="">
                </div>
                
            </div>
            <p class="lead layer">Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio quaerat corrupti, ex delectus distinctio rerum esse eum sint doloremque est!</p>
            <hr class="my-2">
            <p><a href="#"> Info utili</a></p>
            <p class="lead">
                <a class="btn btn-primary btn-lg" href="Jumbo action link" role="button">Scopri di più</a>
            </p>
        </div>
    </div>

</template>

<script>
export default {
    name: 'BannerComponent'
}
</script>

<style lang="scss" scoped>

.landscape {
    background-image: url('https://cdn.pixabay.com/photo/2015/06/19/21/24/avenue-815297_1280.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    h1 {
        -webkit-text-stroke: 2px black;
    }
    .logo {
        border-radius: 50%;
        box-shadow: 0 0 20px 15px black;
    }
    .layer {
        background-color: rgba(0, 0, 0, 0.675);
        border-radius: 0.5rem;
    }
}

</style>