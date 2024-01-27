<script setup>
    defineProps({
        id: Number,
        title: String,
        imageUrl: String,
        price: Number
    })
</script>

<template>
    <div class="flex items-center border border-slate-200 p-4 rounded-xl gap-4">
        <img class="w-16 h-16" :src="imageUrl" :alt="title">

        <div class="flex flex-col">
            <p>{{ title }}</p>
            
            <div class="flex justify-between mt-2">
                <b>{{ price }}</b>
                <img class="opacity-50 hover:opacity-100 cursor-pointer transition" src="/close.svg" alt="Close button">
            </div>
        </div>
    </div>
</template>