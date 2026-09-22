<template>
<div class="mt-15">
    <h3>{{ title }}</h3>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-5 lg:mt-10">
        <div class="order-2 lg:order-1">
            <div class="aspect-[16/11] flex items-center justify-center">
                <img :src="imageUrl1" :alt="imageAlt1" class="rounded-md cursor-pointer" @click="openModal(imageUrl1, imageAlt1)">
            </div>
        </div>
        <div class="order-1 lg:order-2">
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
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-2 mt-2 lg:mt-5">
        <div>
            <div class="aspect-[16/11] flex items-center justify-center">
                <img :src="imageUrl2"  :alt="imageAlt2" class="rounded-md cursor-pointer" @click="openModal(imageUrl2, imageAlt2)">
            </div>
        </div>
        <div>
            <div class="aspect-[16/11] flex items-center justify-center">
                <img :src="imageUrl3"  :alt="imageAlt3" class="rounded-md cursor-pointer" @click="openModal(imageUrl3, imageAlt3)">
            </div>
        </div>
        <div>
            <div class="aspect-[16/11] flex items-center justify-center">
                <img :src="imageUrl4" :alt="imageAlt4" class="rounded-md cursor-pointer" @click="openModal(imageUrl4, imageAlt4)">
            </div>
        </div>
    </div>

    <Teleport to="body">
        <Transition
            enter-active-class="transition-opacity duration-200 ease-out"
            enter-from-class="opacity-0"
            enter-to-class="opacity-100"
            leave-active-class="transition-opacity duration-150 ease-in"
            leave-from-class="opacity-100"
            leave-to-class="opacity-0"
        >
            <div
                v-if="selectedImage"
                class="fixed inset-0 z-50 flex items-center justify-center bg-black/80 backdrop-blur-sm p-4"
                @click.self="closeModal"
            >
                <button
                    class="absolute top-5 right-5 text-white/80 hover:text-white text-3xl font-light focus:outline-none"
                    aria-label="Close image popup"
                    @click="closeModal"
                >
                    &times;
                </button>

                <img
                    :src="selectedImage.url"
                    :alt="selectedImage.alt"
                    class="max-w-full max-h-[90vh] object-contain rounded-md"
                >
            </div>
        </Transition>
    </Teleport>
</div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Tag from '../atoms/Tag.vue'
import LinkIcon from '../icons/LinkIcon.vue'

defineProps({
    title: { type: String },
    description: { type: String },
    tags: { type: Array },
    projectUrl: { type: String },
    imageUrl1: { type: String },
    imageUrl2: { type: String },
    imageUrl3: { type: String },
    imageUrl4: { type: String },
    imageAlt1: { type: String },
    imageAlt2: { type: String },
    imageAlt3: { type: String },
    imageAlt4: { type: String }
});

const selectedImage = ref(null);

const openModal = (url, alt) => {
    if (!url) return;
    selectedImage.value = { url, alt };
};

const closeModal = () => {
    selectedImage.value = null;
};

const handleKeyDown = (e) => {
    if (e.key === 'Escape' && selectedImage.value) {
        closeModal();
    }
};

onMounted(() => window.addEventListener('keydown', handleKeyDown));
onUnmounted(() => window.removeEventListener('keydown', handleKeyDown));
</script>