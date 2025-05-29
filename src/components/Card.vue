<script setup lang="ts">
import { defineProps } from 'vue';
import ListPill from './Listpill.vue';

const props = defineProps({
    title: {
        type: String,
        required: true
    },
    subtitle: {
        type: String,
        required: false
    },
    duration: {
        type: String,
        required: false
    },
    descriptions: {
        type: Array as () => string[],
        required: true
    },
    tools: {
        type: Array as () => { name: string; icon: string }[],
        required: true
    },
    demo: {
        type: String,
        required: false
    },
    code: {
        type: String,
        required: false
    }
});
</script>

<template>
    <div class="card">
        <div class="header">
            <div class="title">
                <h1>{{ props.title }}</h1>
            </div>
            <div class="links">
                <a v-if="props.demo" :href="props.demo" target="_blank" class="btn">Demo<span><font-awesome-icon icon="fa-solid fa-desktop" /></span></a>
                <a v-if="props.code" :href="props.code" target="_blank" class="btn">Github<span><font-awesome-icon icon="fa-brands fa-github" /></span></a>
            </div>
        </div>
        <div class="description">
            <h2 v-if="props.subtitle">{{ props.subtitle }}</h2>
            <h3 v-if="props.duration">{{ props.duration }}</h3>
        </div>
        <div>
            <ul class="descriptions-list">
                <li v-for="(desc, index) in props.descriptions" :key="index">{{ desc }}</li>
            </ul>
        </div>
        <div class="tools">
            <h4>Tools Used:</h4>
            <ListPill :items="props.tools" />
        </div>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    row-gap: 30px;
    width: 100%;
    background: #161616;
    padding: 30px;
    color: #f1f1f1;
    border-radius: 10px;
    box-shadow: 0px 0px 10px #060606;
    line-height: 2rem;
}

.card:hover {
    box-shadow: 0px 5px 10px #bb80ff;
    transition: 0.3s ease-in-out;
}

.card h1 {
    font-size: 2rem;
}

.card h2 {
    font-size: 1.5rem;
    color: #bb80ff;
}

.card h3 {
    font-size: 1.2rem;
    color: #a6a6a6;
}
.card p {
    font-size: 1.2rem;
    margin: 5px 0 5px 0;
}

.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.descriptions-list {
    margin-left: 15px;
    font-size: 1.1rem;
    line-height: 2rem;
}

.tools {
    width: fit-content;
}

.tools h4 {
    font-size: 1.3rem;
    margin-bottom: 10px;
}

hr {
    border: solid 1px #bb80ff;
    margin: 20px 0;
    box-shadow: 0px 0px 10px #bb80ff;
}

.links {
    display: flex;
    row-gap: 10px;
    column-gap: 10px;
}

.btn {
    display: flex;
    align-items: center;
    width: fit-content;
    height: fit-content;
    padding: 3px 10px 3px 10px;
    font-size: 1rem;
    font-weight: 600;
    text-decoration: none;
    color: #f1f1f1;
    background-color: #8e44e2;
    border: none;
    border-radius: 20px;
    cursor: pointer;
}

.btn span {
    display: flex;
    align-items: center;
    margin-left: 5px;
}

.btn span img{
    width: 25px;
    position: relative;
    top: 3px;
    font-size: 1rem;
}

.btn:hover {
    box-shadow: 0px 0px 20px #8e44e2;
    transition: 0.3s;
}
</style>