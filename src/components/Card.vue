<template>
    <div class="card">
        <h2>{{ cardData.title }}</h2>
        <button @click="emitClickEvent">
            <slot name="button-text"></slot>
        </button>
    </div>
</template>

<script>
export default {
    props: {
            cardData: Object,
    },
    methods: {
        emitClickEvent() {
            this.$emit('card-clicked', this.cardData.title);
            }
        }
    }
</script>

<style scoped>
.card {
    border: 1px solid #ccc;
    padding: 15px;
    margin: 10px;
}
</style>