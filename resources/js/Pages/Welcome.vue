<script setup>
import { Head, Link } from '@inertiajs/vue3';
import FrontendLayout from '@/Layouts/Frontend.vue';
import Hero from "@/Components/Frontend/Hero.vue";
import Promote from "@/Components/Frontend/Promote.vue";
import About from "@/Components/Frontend/About.vue";
import Skills from "@/Components/Frontend/Skills.vue";
import Portfolio from "@/Components/Frontend/Portfolio.vue";
import Services from "@/Components/Frontend/Services.vue";
import Contact from "@/Components/Frontend/Contact.vue";

defineProps({
    skills: Object,
    projects: Object,
})
</script>

<template>
    <Head title="Welcome to portfolio" />
    <FrontendLayout>
        <!-- hero  -->
        <Hero />
        <!-- Promote -->
        <Promote />
        <!-- About -->
        <About />
        <!-- Skills -->
        <Skills :skills="skills"/>
        <!-- Portfolio -->
        <Portfolio :skills="skills" :projects="projects" />
        <!-- Services -->
        <Services />
        <!-- Contact -->
        <Contact />
    </FrontendLayout>

</template>

<style>

</style>
