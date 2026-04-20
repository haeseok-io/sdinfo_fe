<template>
    <button :class="classes">
        <slot />
    </button>
</template>

<script setup>
    import { computed } from 'vue';

    const { variant, size } = defineProps({
        variant: { type: String, default: 'primary'},
        size: { type: String, default: 'medium' }
    })

    const base = 'inline-flex items-center justify-center rounded font-medium transition'
    const variants = {
        primary: 'bg-blue-500 text-white hover:bg-blue-600',
        secondary: 'bg-gray-200 text-gray-900 hover:bg-gray-300',
        danger: 'bg-red-500 text-white hover:bg-red-600'
    }
    const sizes = {
        small: 'text-xs px-2.5 py-1',
        medium: 'text-sm px-3 py-1',
        large: 'text-base px-3.5 py-1'
    }

    const classes = computed(() => {
        return [
            base,
            variants[variant] || variants.primary,
            sizes[size] || sizes.medium
        ].join(' ')
    })
</script>