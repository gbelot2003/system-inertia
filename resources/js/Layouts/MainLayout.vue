<script setup>
import { ref } from 'vue';
import { Inertia } from '@inertiajs/inertia';
import { Head, Link } from '@inertiajs/inertia-vue3';
import Navbar from './components/Navbar.vue'
import Cols from './components/Cols.vue'

const logout = () => {
    Inertia.post(route('logout'));
};
</script>
<template>
    <div class="flex h-screen">
        <Navbar />
        <!-- Contenido central -->
        <div class="w-full px-4 py-2 bg-gray-200 lg:w-full">
            <div class="container mx-auto mt-12">
                <div class="grid gap-4 lg:grid-cols-3">
                    <Cols />
                </div>
                <div class="flex flex-col mt-8">
                    <div class="py-2 -my-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
                        <div
                            class="inline-block min-w-full overflow-hidden align-middle border-b border-gray-200 shadow sm:rounded-lg">
                            <slot />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
