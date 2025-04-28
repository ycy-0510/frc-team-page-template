<template>
    <header class="text-black sticky top-0 z-20 bg-slate-200/30 backdrop-blur border border-slate-500/20 px-5 py-3">
        <nav class="flex justify-between items-center container mx-auto ">
            <!-- Logo/Title -->
            <h1 class="text-3xl font-bold tracking-wide italic">FRC####</h1>
            <div class="flex-row space-x-6 md:flex hidden">
                <RouterLink to="/" class="hover:text-sky-500 transition-colors">Home</RouterLink>
                <RouterLink to="/about" class="hover:text-sky-500 transition-colors">About</RouterLink>
                <RouterLink to="/member" class="hover:text-sky-500 transition-colors">Member</RouterLink>
                <RouterLink to="/robots" class="hover:text-sky-500 transition-colors">Robots</RouterLink>
                <RouterLink to="/contact" class="hover:text-sky-500 transition-colors">Contact Us</RouterLink>
            </div>
            <!-- Hamburger Icon for mobile -->
            <div class="block md:hidden">
                <button @click="toggleMenu" class="text-2xl">
                    <font-awesome-icon :icon="['fas', 'bars']" />
                </button>
            </div>
        </nav>
    </header>
    <!-- Mobile Menu -->
    <div class="md:hidden z-15 fixed left-0 top-0 h-screen w-screen bg-slate-200/50 backdrop-blur transition-all duration-300" :class="{'-translate-y-full opacity-20': !menuOpen }">
        <div class="flex justify-end p-5">
            <button @click="toggleMenu" class="text-2xl">
                <font-awesome-icon :icon="['fas', 'times']" />
            </button>
        </div>
        <nav class="flex flex-col items-center space-y-6 mt-10">
            <RouterLink to="/" class="text-black text-xl hover:text-sky-500" @click="toggleMenu">Home</RouterLink>
            <RouterLink to="/about" class="text-black text-xl hover:text-sky-500" @click="toggleMenu">About</RouterLink>
            <RouterLink to="/member" class="text-black text-xl hover:text-sky-500" @click="toggleMenu">Member</RouterLink>
            <RouterLink to="/robots" class="text-black text-xl hover:text-sky-500" @click="toggleMenu">Robots</RouterLink>
            <RouterLink to="/contact" class="text-black text-xl hover:text-sky-500" @click="toggleMenu">Contact Us</RouterLink>
        </nav>

    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// State to toggle the menu
const menuOpen = ref(false)

// Function to toggle menu visibility on mobile
const toggleMenu = () => {
    menuOpen.value = !menuOpen.value
}
</script>

<style scoped>
/* Optional: add some styling for the toggle button */
button {
    background: transparent;
    border: none;
}
</style>