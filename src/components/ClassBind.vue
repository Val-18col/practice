<template>
    <p v-bind:class="{backgroundColor : '#ccc', color: c}">El mensaje se ha enviado satisfactoriamente.</p>
    <button @click="handleClick()">Cambiar color</button>
</template>

<script lang="ts">
    import { defineComponent, ref } from 'vue'
    export default defineComponent({
        name: 'ClassBind',
        setup() {
            let c = ref('#fff')
            const handleClick = () => {c.value = '#ff0000'}
            return {c,handleClick}
    }
})
</script>

<style>

</style>