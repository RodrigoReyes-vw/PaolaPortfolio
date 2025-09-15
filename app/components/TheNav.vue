<script setup lang="ts">
const { data } = await useAsyncData(() => queryCollection('content').all())


</script>
<template>
        <nav class="w-full  bg-gray-200 flex items-center justify-center bg-slate-800 text-white">
           
            <ul class="flex space-x-4 p-4">
                <li v-for="item in data" :key="item._id">
                    <NuxtLink :to="item.path" class="hover:underline">
                        {{ item.title }}
                    </NuxtLink>
                </li>
            </ul>
    </nav>
</template>
<stile>

</stile>