<template>
<section id="ux-ui">
    <h2>UX/UI Design Projects</h2>
    <ProjectCardSlider
        title="Prototype Forest App"
        description="As part of a semester project, a randomly selected mobile application was redesigned in terms of
        UX and UI design. The project focused on the redesign of the “Forest: Focus for Productivity” app by SEEKRTECH CO.
        LTD.. This project included the development of various paper prototypes and the creation and execution of a user testing plan."
        :tags="['Figma', 'Pen & Paper :)']"
        projectUrl="https://www.figma.com/proto/7LuRQjrlIRPWKOz9LfrbDp/Prototype-Forest-App?node-id=4-4&t=ZuSLrFFHspHr1vID-1"
        :images="[
            { url: '/images/forest/forest_crazy8-1.png', alt: 'First Crazy 8 sketch showing an early Forest app concept' },
            { url: '/images/forest/forest_crazy8-2.png', alt: 'Second Crazy 8 sketch showing an early Forest app concept' },
            { url: '/images/forest/forest_crazy8-3.png', alt: 'Third Crazy 8 sketch showing an early Forest app concept' },
            { url: '/images/forest/forest_crazy8-4.png', alt: 'Fourth Crazy 8 sketch showing an early Forest app concept' },
            { url: '/images/forest/forest_paperprototype-1.png', alt: 'First paper prototype of an early Forest app interface' },
            { url: '/images/forest/forest_paperprototype-2.png', alt: 'Second paper prototype of an early Forest app interface' },
            { url: '/images/forest/forest_figma_prototype1.png', alt: 'Forest app prototype in Figma showing the home and forest screens' },
            { url: '/images/forest/forest_figma_prototype2.png', alt: 'Forest app prototype in Figma showing the Friends and Focus Together sections' },
            { url: '/images/forest/forest_figma_prototype3.png', alt: 'Forest app prototype in Figma showing the Profile and Shop sections' }
        ]"
    />
</section>
</template>

<script setup>
import ProjectCardSlider from './templates/ProjectCardSlider.vue'
</script>