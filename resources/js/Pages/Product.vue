<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
import { toRefs, computed } from 'vue'


const props = defineProps({product: Object});
const { product } = toRefs(props)


</script>

<template>
    <Head title="Product" />

    <AuthenticatedLayout>
        <div class="mt-16"></div>

        <div class="max-w-[1200px] mx-auto flex gap-4 justify-between">
            <div class="w-2/5">
                <img :src="product.image">
            </div>
            <div class="w-2/5">
                <div class="text-xl font-extrabold border-b border-b-gray-300 mb-2 pb-2">{{ product.title }}</div>
                <div>
                    <div class="text-lg font-extrabold m-1"> About this item </div>
                    <div> {{ product.description }} </div>
                </div>
            </div>
            <div class="w-1/5">
                <div class="border border-gray-300 rounded-lg">
                    <div class="my-2 mx-3 mb-2">
                        <div class="flex items-center justify-center border-b border-gray-300 pb-1">
                            
                        </div>
                        <div class="flex items-center justify-between pt-2">
                            <div class="text-red-600 text-sm font-bold">${{ product.price }}</div>
                          
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>


