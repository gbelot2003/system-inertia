<script setup>
import SearchField from './SearchField.vue'
import LinkButton from './LinkButton.vue';

const menus = [
    {id: 1, 'name': 'Dashboard', 'url': '/dashboard', 'icon': '🏠'},
    {id: 2, 'name': 'User Profile', 'url': '/user/profile', 'icon': '👥'},
    {id: 3, 'name': 'Logout', 'url': '/logout', 'icon': '👥', method: 'post'},
];

</script>

<template>
    <!-- Menu lateral -->
    <div class="px-4 py-2 bg-blue-600 lg:w-1/4 lg:h-full">
        <svg xmlns="http://www.w3.org/2000/svg" class="inline w-8 h-8 text-white lg:hidden" fill="none"
            viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <div class="hidden lg:block">
            <div class="my-2 mb-6">
                <h1 class="text-2xl font-bold text-white">Admin Dashboard</h1>
            </div>
            <SearchField />
            <ul>
                <LinkButton v-for="menu in menus" :url="menu.url" :icon="menu.name" :method="menu.method" :key="menu.id"></LinkButton>
            </ul>
        </div>
    </div>
    <!-- Menu lateral -->
</template>
