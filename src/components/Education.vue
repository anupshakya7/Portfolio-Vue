<template>
    <div class="w-full">
        <h2 class="text-4xl font-bold mb-4 text-center" data-aos="fade-left">Education</h2>
        <div class="space-y-16 py-14">
            <div class="space-y-16 py-14">
                <div v-for="element in Education" :key="element.id" data-aos="fade-left"
                    class="flex items-center rounded-xl bg-white/75">
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/ios-glyphs/60/graduation-cap--v1.png" alt="graduation">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="uppercase font-semibold text-primary text-base">{{ element.degree }}</h3>
                        <p class="text-gray-500">{{ element.school }}</p>
                        <p class="text-gray-500">{{ element.duration }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const Education = ref([
    { id: 1, degree: 'Software Engineer', school: 'School 1', duration: '2018-2020' },
    { id: 2, degree: 'Frontend Developer', school: 'School 2', duration: '2015-2017' },
    { id: 3, degree: 'Backend Developer', school: 'School 3', duration: '2013-2015' },
]) 
</script>