<template>
    <h1>Trevor Martin - Software Developer</h1>
    <TextContent text-content="A short description of who I am." />
    <ul v-for="project in projects">
        <li>
            <ProjectWithDescription :title="project.title" :link="project.link" :source-link="project.sourceLink" :content="project.content" />
        </li>
    </ul>
</template>

<script setup lang="ts">
import TextContent from './TextContent.vue';
import ProjectWithDescription from './ProjectWithDescription.vue';
import type ProjectContents from '@/types/ProjectContents';

const projects: ProjectContents[] = [
    { title: "J! Scorekeeper", sourceLink: "https://github.com/tcmartin5000/jscorekeeper", link: "https://github.com/tcmartin5000/jscorekeeper/releases/tag/v1.0.0", content: "An Android app written in Kotlin using the new Jetpack Compose declarative UI framework that allows users to play along with the popular TV quiz show. The app supports different versions of the show from around the world, and stores past game results so users can look back at their stats whenever they like." },
    { title: "Wavin' Dave", sourceLink: "https://github.com/tcmartin5000/WavinDave", content: "A rudimentary game written in C for the Nintendo Game Boy using the GBDK 2020 library. Players control Dave and must run toward his neighbors and wave at them to score points. Leave somebody waiting for too long and it's game over!" },
    { title: "Snake", sourceLink: "https://github.com/marttrev/Snake350", content: "A basic version of the classic game Snake written in Java. As a final project for Intro to Software Engineering, our team used this project to learn agile development processes. Over the course of a semester divided into several sprints, we architected, developed, tested, and documented this project." },
    { title: "Untitled Game", sourceLink: "https://github.com/marttrev/376physgame", content: "A game built using C++ and integrating the Box2D physics library written as a team project for Game Programming Techniques. The goal of the game is for each player to cause the other to run into the spikes and take damage enough times that they explode. This project served as an intro to the basics of game engines. It also taught us how to work with third-party libraries in C++."},
    { title: "Trivia Game", link: "https://untitled-trivia-game.vercel.app/", content: "A trivia game made in Vue as a final group project for Web Application Programming. The app has multi-page navigation with Vue Router and integrates account authentication and data storage with Firebase."},
    { title: "Lingo (in progress)", content: "A version of the Dutch game show Lingo built with C# in the Unity game engine. Less a game and more a controller for hosting a game, this project covers the traditional Lingo gameplay, the puzzlewords, and Bonus Lingo."},
    { title: "Bloons FPS", sourceLink: "https://github.com/DeceptiveMagic/CIS376_UnityGame", content: "A first person spin on the classic web game Bloons Tower Defense built using the Unity game engine as a final group project for Game Programming Techniques. We wrote a number of controller scripts and integrated animation, physics, and AI."},
    { title: "This website!", sourceLink: "https://github.com/tcmartin5000/PortfolioWebsite", content: "A basic portfolio website built using Vue to showcase who I am and some of the projects I've worked on over the years. You're looking at it right now!"}
]
</script>

<style></style>