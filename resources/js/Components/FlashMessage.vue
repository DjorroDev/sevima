<template>
    <div
        class="mt-4 border-l-4 px-4 py-2"
        :class="
            type === 'error'
                ? 'border-red-500 bg-red-100 text-red-700'
                : 'border-green-500 bg-green-100 text-green-700'
        "
        role="alert"
    >
        <p class="font-bold uppercase">{{ type }}!</p>
        <p><slot /></p>
    </div>
</template>

<script setup>
defineProps({
    type: String,
});
</script>
