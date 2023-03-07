<template>
    <div class="page">
        <main class="main">
            <div class="container">
                <section class="head">
                    <h1 class="head__title"></h1>
                    <span class="head__subtitle"></span>
                </section>
                <section class="content">
                    <quote-component :image="image.seneca" subText="Сенека Луций Анней (4 г. до н.э. – 65 г. н.э.)"/>
                </section>
            </div>
        </main>
    </div>
</template>
<script setup>
import quoteComponent from '../ui/quoteComponent.vue';
import seneca from '../assets/seneca.png'

const image = {
    seneca
}

</script>
<style lang="sass">

.content
    width: 100%

</style>