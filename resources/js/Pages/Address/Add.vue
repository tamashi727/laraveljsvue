<script setup >

import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';

import InputLabel from '@/Components/InputLabel.vue';
import TextInput from '@/Components/TextInput.vue';
import { toRefs, computed } from 'vue'
import MapMarkerOutlineIcon from 'vue-material-design-icons/MapMarkerOutline.vue'

import PlusIcon from 'vue-material-design-icons/Plus.vue'


let show=true


</script>

<template>
    <Head title="Address" />
    <AuthenticatedLayout>
        <div class="mt-8"></div>
        <div class="w-[500px] mx-auto text-2xl font-extrabold">
            <div>Add A New Address</div>
            <form>
                <div class="text-[15px] -mb-1.5 font-extrabold">Country</div>
                <select class="w-full border-gray-300 rounded-lg shadow-md py-1 bg-gray-200 hover:bg-gray-300 
                cursor-pointer 
                focus:border-orange-400 focus:ring-orange-300" name="country">
                    <option selected value="united kingdom">United Kingdom</option>
                    <option value="united states">United states</option>
                    <option value="germany">germany</option>
                    <option value="france">United Kingdom</option>
                </select>

                <div class="mt-4">
                    <InputLabel class="-mb-1.5" value="First name" />

                    <TextInput
                        
                        type="text"
                        class="mt-1 block w-full"
                        required
                    />
                </div>

                <div class="mt-3">
                    <InputLabel class="-mb-1.5" value="Last name" />

                    <TextInput
                        
                        type="text"
                        class="mt-1 block w-full"
                        required
                    />
                </div>

                <div class="mt-3">
                    <InputLabel class="-mb-1.5" value="Address" />

                    <TextInput
                        type="text"
                    
                        class="mt-1 block w-full"
                        required
                        placeholder="Address line 1"
                    />

                    <TextInput
                        type="text"
                        
                        class="mt-1 block w-full"
                        required
                        placeholder="Address line 2"
                    />
                </div>

                <div class="mt-3">
                    <div class="flex gap-2">
                        <div class="w-full">
                            <InputLabel class="-mb-1.5" value="City" />

                            <TextInput
                                type="text"
                                
                                class="mt-1 block w-full"
                                required
                                placeholder="City"
                            />
                        </div>

                        <div class="w-full">
                            <InputLabel class="-mb-1.5" value="Postcode" />

                            <TextInput
                                type="text"
                                
                                class="mt-1 block w-full"
                                required
                                placeholder="Postcode"
                            />
                        </div>
                    </div>
                </div>

                <div class="mt-6">
                    <button class="bg-yellow-400 px-3 font-bold text-[14px] rounded-lg shadow-sm cursor-pointer">
                        Add address
                    </button>
                </div>

            </form>
        </div>
    </AuthenticatedLayout>

</template>

