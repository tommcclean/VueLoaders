<template functional>
    <button v-bind:class="[{'no-events': props.isLoading}]">
        <slot/>
        <p>{{props.text}}</p>
    </button>
</template>

<script>
export default {
    name: "loading-button",
    props: {
        text: {
            type: String,
            default: "Submit"
        },
        isLoading: {
            type: Boolean,
            default: false
        }
    }
};
</script>

<style scoped>
button img {
    width: 20px;
    height: 20px;
}
button p {
    display: inline-block;
    margin: 0;
}

.no-events{
    user-select: none;
    pointer-events: none;
}
</style>