<template>
    <button :class="classes">
        <slot />
    </button>
</template>

<script setup>
    import { computed } from 'vue';

    const props = defineProps({
        variant: {type: String, default: 'primary'},
        size: {type: String, default: 'medium'}
    })

    const classes = computed(() => [
        'button',
        `button--${props.variant}`,
        `button--${props.size}`
    ])
</script>