<template>
    <div class="main">
        <vBanner/>
        <div class="form-container">
            <vMainForm/>
        </div>
    </div>
</template>

<script>
import vBanner from './v-banner.vue';
//import vMainForm from './v-main-form.vue';
import vMainForm from './v-main-form.vue';

export default {
    name: 'v-main-wrapper',
    components: {
        vBanner,
        vMainForm,
    }
}
</script>

<style>
.form-container {
    max-width: 1236px;
    padding: 24px 0;
    margin: auto;
}
</style>