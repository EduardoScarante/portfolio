<script>

export default {
    props: {
        data: String,
        path: String,
        subtitle: String
    }
}
</script>


<template>
    <div class="card">
        <div class="imgCard">
            <img :src="path" alt="">
        </div>
        <div class="title">
            <div class="data">
                {{ data }}
            </div>
            <div class="des">
                {{ subtitle }}
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;

    margin: 10px;

    height: 180px;
    width: 180px;

    box-shadow: 3px 3px 3px rgb(7, 7, 7);
    border-radius: 20px;
    background-color: rgba(0, 0, 0, 0.2);
    transition: 0.6s ease-in-out;

}

img {
    height: 70px;
    width: 125px;
    border-radius: 10px;
    margin-bottom: 10px;

    box-shadow: 2px 2px 5px black;
}

.imgCard {
    width: 100%;

    display: flex;
    justify-content: center;
    align-items: center;
}

.card:hover {
    box-shadow: 0px 0px 3px rgb(255, 255, 255);
}

.data{
    font-weight: 800;
    padding-top: 10px;
}
.des{
    font-weight: 400;
}
</style>
