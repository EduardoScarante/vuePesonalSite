<script>

export default {
    props: {
        data: String
    }
}
</script>


<template>
    <div class="card">
        <img :src="img" alt="">
        {{ data }}
    </div>
</template>

<style>
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;

    margin: 10px;

    height: 200px;
    width: 200px;

    box-shadow: 3px 3px 3px rgb(7, 7, 7);
    border-radius: 20px;
    background-color: #212121;
    transition: 0.6s ease-in-out;

    padding: 25px;

}

.card:hover {
    box-shadow: 0px 0px 3px rgb(253, 253, 253);
}
</style>
