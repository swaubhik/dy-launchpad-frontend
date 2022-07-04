<template>
    <button>
        {{ msg }}
        <slot />
    </button>
</template>
<script>

export default {
    name: "Button",
    props: {
        msg: String,
    },
};
</script>
<style lang="scss">
</style>