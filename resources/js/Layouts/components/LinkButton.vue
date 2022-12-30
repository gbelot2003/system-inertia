<script setup>
import { Link } from '@inertiajs/inertia-vue3';

const props = defineProps({
    url: String,
    icon: String,
    method: String
})

</script>

<template>
    <li class="mb-1 rounded hover:shadow hover:bg-gray-800">
        <Link :href="props.url" :method="props.method" class="inline-block w-full h-full px-3 py-2 font-bold text-white rounded">
            {{ props.icon }}
            <slot />
        </Link>
    </li>
</template>
