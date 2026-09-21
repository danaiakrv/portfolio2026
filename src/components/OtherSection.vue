<template>
<section id="other">
    <h2>Other Projects</h2>
    <ProjectCardLeft
        title="Diplomaproject 2020"
        description='"Where Is Eleanor Rose?" is a combination of a 2D adventure game and visual novel that represents
        the grieving process through the five stages of grief, first introduced by Elisabeth Kübler-Ross. Georgia Daisy,
        a young schoolgirl, searches for her missing friend Eleanor Rose and faces many challenges as the game progresses.
        My part of this diploma project focused on exploring how the five stages of grief can be represented through level
        and asset design.'
        :tags="['Unity', 'C#', 'CC Photoshop', 'Sourcetree/Git']"
        projectUrl="https://kinayastudios.itch.io/where-is-eleanor-rose"
        imageUrl1="/images/diploma/eleanor_promo2_cropped.jpg"
        imageUrl2="/images/diploma/frame_diplomaproj2.png"
        imageUrl3="/images/diploma/frame_diplomaproj3.png"
        imageUrl4="/images/diploma/frame_diplomaproj4.png"
        imageAlt1='Promotional visual for "Where Is Eleanor Rose?"'
        imageAlt2="Game screenshot representing Stage Anger"
        imageAlt3="Game screenshot representing Stage Depression"
        imageAlt4="Game screenshot representing Stage Bargaining"
    />
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
import ProjectCardLeft from './templates/ProjectCardLeft.vue'
import ProjectCardSlider from './templates/ProjectCardSlider.vue'
</script>