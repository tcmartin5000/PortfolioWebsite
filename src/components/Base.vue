<template>
    <div>
        
            <li v-for="project in projects" :key="project.id">
                <ProjectWithDescription :ms-delay="msDelay * project.id" :project-contents="project" />
            </li>
        

    </div>
</template>

<script setup lang="ts">
import ProjectWithDescription from './ProjectWithDescription.vue';
import type ProjectContents from '@/types/ProjectContents';
import { ref, onBeforeMount, onMounted, type Ref } from 'vue';

const props = defineProps<{
    parentHeight: number
}>()

const projects: Ref<ProjectContents[]> = ref([]);
const msDelay: number = 200

onMounted(() => {
    projects.value.push(
        { id: 0, title: "J! Scorekeeper", sourceLink: "https://github.com/tcmartin5000/jscorekeeper", link: "https://github.com/tcmartin5000/jscorekeeper/releases/tag/v1.0.0", content: "An Android app written in Kotlin using the new Jetpack Compose declarative UI framework that allows users to play along with the popular TV quiz show. The app supports different versions of the show from around the world, and stores past game results so users can look back at their stats whenever they like." },
        { id: 1, title: "Grady's Garden web app overhaul", link: "https://drive.google.com/file/d/1Oo3uW3eZiK3NFe-j3siuGSN_pIDtsJUf/view?usp=sharing", content: "My senior project at Grand Valley State University, our team was assigned to work with the nonprofit organization Grady's Garden to help build out an educational web app. We utilized AWS services to build out a database to store user data for later analysis, and refactored their Vue-based web app to interact with that database. We also helped them recover some of their source code, which the non-technical project coordinators were unaware was missing." },
        { id: 2, title: "Trivia Game", link: "https://untitled-trivia-game.vercel.app/", content: "A trivia game made in Vue as a final group project for Web Application Programming. The app has multi-page navigation with Vue Router and integrates account authentication and data storage with Firebase." },
        { id: 3, title: "Lingo (in progress)", link: "https://youtu.be/ka6vIOhVmyI?si=J8NljYK2ldJoHv64", content: "A version of the Dutch game show Lingo built with C# in the Unity game engine. Less a game and more a controller for hosting a game, this project covers the traditional Lingo gameplay, the puzzlewords, and Bonus Lingo." },
        { id: 4, title: "Wavin' Dave", sourceLink: "https://github.com/tcmartin5000/WavinDave", content: "A rudimentary game written in C for the Nintendo Game Boy using the GBDK 2020 library. Players control Dave and must run toward his neighbors and wave at them to score points. Leave somebody waiting for too long and it's game over!" },
        { id: 5, title: "Snake", sourceLink: "https://github.com/marttrev/Snake350", content: "A basic version of the classic game Snake written in Java. As a final project for Intro to Software Engineering, our team used this project to learn agile development processes. Over the course of a semester divided into several sprints, we architected, developed, tested, and documented this project." },
        { id: 6, title: "Untitled Game", sourceLink: "https://github.com/marttrev/376physgame", content: "A game built using C++ and integrating the Box2D physics library written as a team project for Game Programming Techniques. The goal of the game is for each player to cause the other to run into the spikes and take damage enough times that they explode. This project served as an intro to the basics of game engines. It also taught us how to work with third-party libraries in C++." },
        { id: 7, title: "Bloons FPS", sourceLink: "https://github.com/DeceptiveMagic/CIS376_UnityGame", content: "A first person spin on the classic web game Bloons Tower Defense built using the Unity game engine as a final group project for Game Programming Techniques. We wrote a number of controller scripts and integrated animation, physics, and AI." },
        { id: 8, title: "Three.js demo", link: "https://student.computing.gvsu.edu/marttrev/hw3/index.html", content: "A basic demo in the web graphics framework Three.js demonstrating movement of textured objects and adjustment of lighting and camera positioning." },
        { id: 9, title: "WebGL demo", link: "https://student.computing.gvsu.edu/marttrev/hw2.2/Extension/sierpinski-extended.html", content: "A basic graphics demo using WebGL technologies demonstrating the usage of vertex and fragment shaders to produce a rotating fractal. Colors can be changed using the R, G, B, and space bar keys, and the shape of the image can be changed using the controls visible on the page as well as by clicking into the canvas." },
        { id: 10, title: "This website!", sourceLink: "https://github.com/tcmartin5000/PortfolioWebsite", content: "A basic portfolio website built using Vue to showcase who I am and some of the projects I've worked on over the years. You're looking at it right now!" }
    )

})

</script>

<style scoped>
li {
    list-style-type: none;
}

</style>