<template>
<section id="frontend">
    <h2>Frontend Development Projects</h2>
    <ProjectCardLeft
        title="Bachelorproject 2026"
        description="This thesis explores how front-end style guides can support accessibility and usability in web
        applications. A front-end style guide and evaluation artifacts were developed and tested using accessibility
        and usability testing. The results showed slight differences between applications based on the two approaches."
        :tags="['Angular', 'TypeScript', 'SCSS', 'PrimeNG', 'Git']"
        projectUrl="https://github.com/danaiakrv/frontend-style-guide-evaluation"
        imageUrl1="/images/bachelor/frame_taiyaki1.png"
        imageUrl2="/images/bachelor/frame_taiyaki2.png"
        imageUrl3="/images/bachelor/frame_taiyaki3.png"
        imageUrl4="/images/bachelor/frame_taiyaki4.png"
        imageAlt1="Styleguide homepage design showing the brand identity and layout"
        imageAlt2="Styleguide logo system showing logo variations and construction details"
        imageAlt3="Styleguide colour system showing the brand colour palette"
        imageAlt4="Styleguide table component showing the component layout and styling"
    />
    <ProjectCardRight
        title="Taiyaki Webshop"
        description="This semester project is a responsive webshop for taiyakis, a traditional Japanese dessert.
        The application includes user registration and login, profile management, review creation and management and
        a checkout process."
        :tags="['Vue.js', 'JavaScript', 'CSS', 'Java Spring Boot', 'MySQL', 'Docker', 'Git']"
        projectUrl="https://github.com/viktormandlbauer/taiyaki"
        imageUrl1="/images/taiyakiweb/frame_taiyakiweb1.png"
        imageUrl2="/images/taiyakiweb/frame_taiyakiweb2.png"
        imageUrl3="/images/taiyakiweb/frame_taiyakiweb3.png"
        imageUrl4="/images/taiyakiweb/frame_taiyakiweb4.png"
        imageAlt1="Taiyaki homepage design showing the brand identity and layout"
        imageAlt2="Taiyaki product page showing product details and a customer review"
        imageAlt3="Taiyaki user profile page showing account details"
        imageAlt4="Taiyaki admin page for adding, searching and managing user accounts"
    />
    <ProjectCardLeft
        title="Plantie House Webshop"
        description="Plantie House is a modern online marketplace where users can browse and purchase a variety of
        plants and accessories. The application includes user registration and login, profile management and a checkout process."
        :tags="['HTML', 'CSS', 'JavaScript', 'Node.js', 'Express', 'SQLite', 'Git']"
        projectUrl="https://github.com/Enquaza/plantie-webshop"
        imageUrl1="/images/plantieweb/frame_plantieweb1.png"
        imageUrl2="/images/plantieweb/frame_plantieweb2.png"
        imageUrl3="/images/plantieweb/frame_plantieweb3.png"
        imageUrl4="/images/plantieweb/frame_plantieweb4.png"
        imageAlt1="Plantie House homepage design showing the brand identity and layout"
        imageAlt2="Taiyaki product page showing multiple products and their details"
        imageAlt3="Taiyaki checkout page showing three products added to the cart"
        imageAlt4="Taiyaki user profile showing orders with an option to view receipts"
    />
</section>
</template>

<script setup>
import ProjectCardLeft from './templates/ProjectCardLeft.vue'
import ProjectCardRight from './templates/ProjectCardRight.vue'
</script>