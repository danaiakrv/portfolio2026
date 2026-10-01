<template>
<section id="game">
    <h2>Game Development</h2>
    <ProjectCardVideo
        title="Where is Eleanor Rose?"
        description='"Where Is Eleanor Rose?" is a combination of a 2D adventure game and visual novel that represents
        the grieving process through the five stages of grief, first introduced by Elisabeth Kübler-Ross. Georgia Daisy,
        a young schoolgirl, searches for her missing friend Eleanor Rose and faces many challenges as the game progresses.
        My part of this diploma project focused on exploring how the five stages of grief can be represented through level
        and asset design.'
        :tags="['Unity', 'C#', 'CC Photoshop', 'Sourcetree/Git']"
        projectUrl="https://kinayastudios.itch.io/where-is-eleanor-rose"
        vidUrl="https://www.youtube.com/embed/QDef6qkOlhk?si=BDKuoaVPhB7tc-UV"
        imageUrl1="/images/diploma/frame_diplomaproj2.png"
        imageUrl2="/images/diploma/frame_diplomaproj3.png"
        imageUrl3="/images/diploma/frame_diplomaproj4.png"
        imageAlt1="Game screenshot representing Stage Anger"
        imageAlt2="Game screenshot representing Stage Depression"
        imageAlt3="Game screenshot representing Stage Bargaining"
    />
    <ProjectCardRight
        title="Riddle Room VR"
        description="RiddleRoomVR is an Egyptian escape room game that combines physical and virtual worlds. Together,
        the analogue and VR players have to solve mystical puzzles within an ancient tomb. The book given to the analogue
        player provides symbolic solutions to guide the VR player through out of the tomb. My part of this project was
        to develop 2D/3D assets and the handbook for the analogue player."
        :tags="['Unity', 'C#', 'CC Photoshop', 'Autodesk Maya', '3D Substance Painter', 'Sourcetree/Git']"
        imageUrl1="/images/riddleroom/frame_riddleroom1.png"
        imageUrl2="/images/riddleroom/frame_riddleroom2.png"
        imageUrl3="/images/riddleroom/frame_riddleroom3.png"
        imageUrl4="/images/riddleroom/frame_riddleroom4.png"
        imageAlt1="Game screenshot showing the start screen of the game"
        imageAlt2="Game screenshot showing the handbook for the analogue player"
        imageAlt3="Game screenshot showing the player pressing a button"
        imageAlt4="Game screenshot showing the escape room"
    />
</section>
</template>

<script setup>
import ProjectCardVideo from './templates/ProjectCardVideo.vue'
import ProjectCardRight from './templates/ProjectCardRight.vue'
</script>