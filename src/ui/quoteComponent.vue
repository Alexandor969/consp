<template>
    <div class="quote-box">
        <div class="quote__image-box">
            <img :src="image" :alt="image" class="quote__image">
        </div>
        <div class="quote">
            <p class="quote__text" ref="element">Общество – свод из камней, который обрушился бы, если бы один не поддерживал другого.<span class="quote__text_cursor"></span></p>
            <span class="quote__text">Сенека Луций Анней (4 г. до н.э. – 65 г. н.э.)</span>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue'
const props = defineProps({
    image: {
        type: String,
        required: true
    },
    text: {
        type: String,
        required: true
    },
    subText: {
        type: String,
        required: true
    }
})

const element = ref(null)

console.log(element)
console.log(element.value)
console.log(element)

</script>
<style lang="sass">

@keyframes flashing
    0%
        opacity: 1
    50%
        opacity: 0
    100%
        opacity: 1

.quote
    display: block
    max-width: 600px
    width: 100%
    padding: 20px 10px
    border: 1px solid var(--green)
    &-box
        margin: 0 auto
        display: flex
        align-items: flex-start
        max-width: 700px
        width: 100%
        gap: 20px
    &__image
        display: block
        width: 100%
        height: 100%
        background-color: var(--white)
        object-position: center center
        &-box
            display: block
            width: 80px
            height: 80px
            border-radius: 50%
            overflow: hidden
            flex: none
    &__text
        display: block
        font-size: 14px
        width: 100%
        font-family: var(--mono)
        &_cursor
            display: inline-block
            width: 6px
            height: 3px
            background-color: var(--white)
            animation: flashing 0.75s infinite step-start
        &:not(:first-child)
            margin-top: 25px
</style>