<template>
    <div class="banner">
        <div class="banner-text">
            <h1>Генератор UTM меток</h1>
            <p>Создайте ссылку для рекламных кампаний Google, Яндекс или других и узнайте, 
                откуда приходят ваши клиенты, и насколько эффективна рекламная кампания.
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "v-banner"
}

</script>

<style>
    .banner {
        background: url('../../assets/img/banner.png');
        background-repeat: no-repeat;
        background-size: cover;
    }

    .banner-text {
        padding: 51px 0 56px 0;
        margin: auto;
        width: 606px;
    }

</style>