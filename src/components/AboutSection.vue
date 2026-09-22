<template>
<section id="about">
    <h2>About me</h2>
    <div class="grid gap-4 grid-cols-1 lg:grid-rows-[auto_1fr] items-start">
      <div class="xl:col-span-2">
        <p class="xl:my-4 lg:mr-10">
          I'm a frontend developer, UX/UI designer and artist. Always looking for new ways to make products more
          intuitive, efficient and enjoyable. I focus on creating visually appealing but also user-friendly applications.
        </p>
      </div>
      <div class="lg:row-start-2 xl:col-span-2 xl:row-span-2 xl:row-start-2">
        <div class="lg:grid lg:grid-cols-2 lg:gap-10">
            <div>
                <h3>My Skills</h3>
                <div class="grid grid-cols-3 gap-3 sm:gap-4">
                    <div class="aspect-square flex flex-col gap-2 items-center justify-center">
                        <img src="/icons/icons_frontend.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">Frontend Development</p>
                    </div>
                    <div class="aspect-square flex flex-col gap-2 items-center justifynpm-center">
                        <img src="/icons/icons_backend.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">Backend Development</p>
                    </div>
                    <div class="aspect-square flex flex-col gap-2 items-center justify-center">
                        <img src="/icons/icons_uxui.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">UX/UI Research & Design</p>
                    </div>
                    <div class="aspect-square flex flex-col gap-2 items-center justify-center">
                        <img src="/icons/icons_art.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">Graphic Design & Art</p>
                    </div>
                    <div class="aspect-square flex flex-col gap-2 items-center justify-center">
                        <img src="/icons/icons_game.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">Game Development</p>
                    </div>
                </div>
            </div>
            <div>
                <h3 class="pt-5 lg:pt-0">Contact</h3>
                <div class="grid grid-cols-3 gap-3 sm:gap-4">
                    <a href="mailto:danaiakrv@gmail.com" target="_blank" rel="noopener noreferrer" aria-label="Email" class="aspect-square flex flex-col gap-2 items-center justify-center !no-underline">
                        <img src="/icons/icons_email.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">E-Mail</p>
                    </a>
                    <a href="https://www.linkedin.com/in/danaiakrv/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn" class="aspect-square flex flex-col gap-2 items-center justify-center !no-underline">
                        <img src="/icons/icons_linkedin.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">LinkedIn</p>
                    </a>
                    <a href="https://github.com/danaiakrv" target="_blank" rel="noopener noreferrer" aria-label="GitHub" class="aspect-square flex flex-col gap-2 items-center justify-center !no-underline">
                        <img src="/icons/icons_github.png" alt="" class="duration-300 hover:scale-105">
                        <p class="!text-xs !text-center">GitHub</p>
                    </a>
                </div>
            </div>
        </div>
      </div>
      <div class="lg:col-start-2 xl:col-start-3 lg:row-span-3 lg:row-start-1 flex justify-center">
        <img src="/images/me.png" alt="" class="w-full max-w-sm lg:w-120 lg:max-w-none mx-auto flex items-center justify-center rounded-xl">
      </div>
    </div>
    <div class="flex items-center justify-center mt-12">
        <button id="scroll-button" class="bg-purple-900 hover:bg-violet-900 h-20 w-80 py-3 px-5 text-white text-lg font-bold uppercase rounded-full flex gap-3 items-center justify-center cursor-pointer duration-300 hover:scale-105">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-8 animate-[bounce_1s_infinite]">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 13.5 12 21m0 0-7.5-7.5M12 21V3" />
            </svg>
            <span>View my work</span>
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-8 animate-[bounce_1s_infinite]">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 13.5 12 21m0 0-7.5-7.5M12 21V3" />
            </svg>
        </button>
    </div>
</section>
</template>

<script setup>
import EnvelopeIcon from './icons/EnvelopeIcon.vue'
import LinkedInIcon from './icons/LinkedInIcon.vue'
import GitHubIcon from './icons/GitHubIcon.vue'


document.addEventListener('DOMContentLoaded', () => {
    const button = document.getElementById('scroll-button');
    const target = document.getElementById('frontend');

    if (button && target) {
        button.addEventListener('click', () => {
            target.scrollIntoView({ behavior: 'smooth' });
        });
    }
});
</script>