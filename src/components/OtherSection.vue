<template>
<section id="other">
    <h2>Other Projects</h2>
    <ProjectCardSlider
        title="Digital and Traditional Art"
        description="Drawing traditionally has been my passion since childhood. Over time, I learned to create my artworks
        in a digital environment as well. Thanks to my school's specialisation, I gained access to professional software
        that allowed me to further develop my drawing and editing skills."
        :tags="['CC Photoshop', 'Clip Studio Paint', 'Sketchbook']"
        :images="[
            { url: '/images/art/cover.png', alt: 'Album cover artwork showing a person holding an umbrella' },
            { url: '/images/art/Chibiusa.png', alt: 'Fan art of Chibiusa from Sailor Moon' },
            { url: '/images/art/frieren_fanart.png', alt: 'Fan art of Frieren from Frieren' },
            { url: '/images/art/LeeJongSuk.jpg', alt: 'Portrait fan art of Korean actor Lee Jong Suk' },
            { url: '/images/art/solgaleo.jpg', alt: 'Realistic fan art of Pokémon Solgaleo' },
            { url: '/images/art/emiyo_fullpalette_favs.png', alt: 'Character design showing different colour palette variations' },
            { url: '/images/art/drawthisinyourstyle.png', alt: 'Attempt of Draw this in your style-challenge by Pernille Oerum' }
        ]"
    />
</section>
</template>

<script setup>
import ProjectCardSlider from './templates/ProjectCardSlider.vue'
</script>