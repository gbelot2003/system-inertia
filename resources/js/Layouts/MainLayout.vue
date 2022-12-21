<script setup>
import { ref } from 'vue';
import { Inertia } from '@inertiajs/inertia';
import { Head, Link } from '@inertiajs/inertia-vue3';

const logout = () => {
    Inertia.post(route('logout'));
};
</script>
<template>
    <main>
        <slot />
    </main>
</template>
