<script setup >

import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
import { toRefs, computed } from 'vue'
import MapMarkerOutlineIcon from 'vue-material-design-icons/MapMarkerOutline.vue'

import PlusIcon from 'vue-material-design-icons/Plus.vue'


let show=true


</script>

<template>
    <Head title="Address" />
    <AuthenticatedLayout>
        <div class="mt-12">

        </div>
        <div class="max-w-[1000px] mx-auto text-3xl mb-10">
            Your Address
            
        </div>
        <div class="max-w-[1000px] mx-auto flex gap-2 h-[270px]">
            <div class="border border-dotted border-gray-400 rounded-md w-1/3">
                <Link v-if="show" href="/">
                    <div class="grid h-full place-items-center cursor-pointer">
    <div class="text-center">
        <div class="flex justify-center">
            <PlusIcon fillColor="#5E5E5E" size="20" />
        </div>
        <div class="font-bold text-2xl">Add Address</div>
    </div>                    
                    </div>
                </Link>
                <div v-else class="grid h-full pace-items-center">
                    <div class="text-center">
                        <div class="font-bold text-2xl">Text Is Added</div>
                    </div>
                </div>
            </div>

            <div class="relative border border-gray-400 rounded-md w-1/3 shadow-md">
                <div class="flex items-center justify-start p-3 text-xs text-gray-600 font-extrabold border-b-gray-400">
                    Default: <img class="h-3 mt-1.5 ml-2" src="/images/logo/AMAZON_LOGO_DARK.png" alt="">
                </div>
                <div class="text-sm font-extrabold px-4 pt-4">
                    FIRST NAME LAST NAME
                </div>
                <div class="text-sm px-4">
                    <div>ADDR 1</div>
                    <div>ADDR 2</div>
                    <div>city</div>
                    <div>postcode</div>
                    <div>country</div>
                </div>
                <div class="px-4 absolute  bottom-0 pb-4">
                    <Link href="/" class="text-teal-700 text-sm font-extrabold hover:underline hover:text-red-700">  Remove       
                    </Link>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>

</template>

