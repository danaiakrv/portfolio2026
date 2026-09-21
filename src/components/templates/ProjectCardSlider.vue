<template>
<div class="mt-15">
    <h3>{{ title }}</h3>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-5">
        <div>
            <p class="mt-3 lg:mr-10">
                {{ description }}
            </p>
            <div v-if="projectUrl" class="flex items-center mt-4">
                <LinkIcon class="mr-2"/>
                <p>
                    <a :href="projectUrl" class="text-purple-800 hover:underline">View Project</a>
                </p>
            </div>
            <p class="mt-3"> Tools used: </p>
            <div v-if="tags?.length" class="flex flex-wrap gap-2 my-4">
                <Tag v-for="tag in tags" :key="tag">{{ tag }}</Tag>
            </div>
        </div>
        <div>
            <div class="relative aspect-[16/11] max-w-2xl mx-auto overflow-hidden rounded-md shadow-lg mt-5">
                <div
                    class="flex h-full transition-transform duration-700 ease-out"
                    :style="{
                        width: `${images.length * 100}%`,
                        transform: `translateX(-${currentIndex * (100 / images.length)}%)`
                    }"
                >
                    <div
                        v-for="(image, index) in images"
                        :key="index"
                        class="h-full flex-shrink-0 flex items-center justify-center"
                        :style="{ width: `${100 / images.length}%` }"
                    >
                        <img :src="image.url" :alt="image.alt" class="w-full h-full object-cover">
                    </div>
                </div>

                <button
                    @click="currentIndex = (currentIndex - 1 + images.length) % images.length"
                    class="absolute left-3 top-1/2 -translate-y-1/2 bg-black/40 hover:bg-black/70 text-white p-2 rounded-full backdrop-blur-sm transition"
                >
                    &#10094;
                </button>
                <button
                    @click="currentIndex = (currentIndex + 1) % images.length"
                    class="absolute right-3 top-1/2 -translate-y-1/2 bg-black/40 hover:bg-black/70 text-white p-2 rounded-full backdrop-blur-sm transition"
                >
                    &#10095;
                </button>
            </div>
            <p v-if="images[currentIndex]" class="text-sm mt-2 text-center">
                {{ images[currentIndex].alt }}
            </p>
        </div>
    </div>
</div>
</template>

<script setup>
import { ref } from 'vue';
import LinkIcon from '../icons/LinkIcon.vue';
import Tag from '../atoms/Tag.vue';

defineProps({
    title: { type: String },
    description: { type: String },
    tags: { type: Array },
    projectUrl: { type: String },
    images: {
        type: Array,
        default: () => []
    }
});

const currentIndex = ref(0);
const totalSlides = 3;

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % totalSlides;
};

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + totalSlides) % totalSlides;
};
</script>