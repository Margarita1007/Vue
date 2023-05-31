<template>
    <div class="header2-nav">
        <div class="header2-nav-link">
            <a href="/">Офферы</a>
            <a href="/">Отчеты</a>
            <a href="/">Мой аккаунт</a>
            <a href="/">Финансы</a>
            <a href="/">Инструменты</a>
            <a href="/">Leads.Market</a>
            <a href="/">Moneyfest</a>
        </div>
        <div class="header2-nav-help">
            <a href="/">? Помощь</a>
        </div>
        

    </div>

</template>

<script>
    export default {
    name: 'v-header-nav'
    }
</script>

<style>
    .header2-nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        max-width: 1236px;
        margin: auto;
        height: 54px;
        border: 1px solid #EBEFF3;
    }

    .header2-nav-link {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 32px;
    }

    .header2-nav-link a {
        text-decoration: none;
        color: black;
    }

    .header2-nav-help {
        display: flex;
        align-items: center;
    }

    .header2-nav-help a {
        text-decoration: none;
        color: black;
    }
</style>