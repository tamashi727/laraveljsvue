<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100">
        <div>
            <Link href="/">
                <img class="h-12 fill-current text-gray-500" src="/images/logo/AMAZON_LOGO_DARK.png" alt="">
            </Link>
        </div>

        <div
            class="w-full sm:max-w-md mt-6 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg"
        >
            <slot />
        </div>
        <div v-if="$page.url === '/login'" class="w-[400px]">
            <div class="text-center text-sm text-gray-600 font-bold py-4">New to Amazon?</div>
            <div class="w-full border border-gray-500 bg-gray-200 text-sm font-extrabold p-2 hover:bg-gray-300 text-center">
                <Link :href="route('register')">
                    Create your Amazon account
                </Link>
            </div>
        </div>
    </div>
</template>
