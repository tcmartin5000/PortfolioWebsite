<template>
    <div>
        <h1>Trevor Martin - Software Developer</h1>
        <div class="separator"></div>
        <p>{{ description }}</p>
        <div class="separator"></div>

        <div class="contact-row">
            <a :href="email" class="icon-block">
                <span class="material-symbols-outlined">
                    mail
                </span>
                <p>Email</p>
            </a>
            <a :href="linkedin" class="icon-block">
                <span class="material-symbols-outlined">
                    work
                </span>
                <p>LinkedIn</p>
            </a>

        </div>



    </div>
</template>

<script setup lang="ts">
const description = "I'm a Computer Science student with four years of classes under my belt. I'm a quick learner with experience in a wide variety of technologies, and I've worked on projects both solo and in teams. On this page, you can see some of my work, including both class assignments and personal projects."
const email = "mailto:contact@trevorcmartin.com"
const linkedin = "https://www.linkedin.com/in/trevor-c-martin/"
</script>

<style scoped>
div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

p {
    text-align: center;
}

h1 {
    text-align: center;
}

.separator {
    margin-top: 10px;
}

.material-symbols-outlined {
    padding-right: 10px;
}

.contact-row {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-evenly;
}

.icon-block {
    display: flex;
    flex-direction: row;
}
</style>