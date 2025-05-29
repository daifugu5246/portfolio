<script setup lang="ts">
import { ref } from 'vue';
import ListPill from './Listpill.vue';

const languages = ref([
    { name: 'Python', icon: '/assets/languages/python.png' },
    { name: 'JavaScript', icon: '/assets/languages/js.png' },
    { name: 'TypeScript', icon: '/assets/languages/typescript.png' },
    { name: 'PHP', icon: '/assets/languages/php.png' },
    { name: 'C#', icon: '/assets/languages/c-sharp.png' },
    { name: 'C/C++', icon: '/assets/languages/cpp.png' },
    { name: 'Java', icon: '/assets/languages/java.png' }
]);

const tools = ref([
    { name: 'React', icon: '/assets/tools/react.png' },
    { name: 'Vue.js', icon: '/assets/tools/vue.svg' },
    { name: 'Bootstrap', icon: '/assets/tools/bootstrap.png' },
    { name: 'Laravel', icon: '/assets/tools/laravel.png' },
    { name: 'Express.js', icon: '/assets/tools/expressjs.png' },
    { name: 'MongoDB', icon: '/assets/tools/mongodb.svg' },
    { name: 'MySQL', icon: '/assets/tools/mysql.png' },
    { name: 'Git', icon: '/assets/tools/git.png' },
    { name: 'Postman', icon: '/assets/tools/postman.svg' },
    { name: 'Docker', icon: '/assets/tools/docker.png' }
]);
</script>

<template>
    <div class="skill" id="skill">
        <div class="header">
            <h1>Skills</h1>
            <hr>
        </div>
        <div class="languages card">
            <h1>Languages</h1>
            <ListPill :items="languages" />
        </div>
        <div class="tools card"> 
            <h1>Tools & Framework</h1>
            <ListPill :items="tools" />
        </div>
    </div>
</template>

<style scoped>
.skill {
    display: grid;
    column-gap: 20px;
    width: 100%;
    height: fit-content;
    padding: 150px 300px 150px 300px;
    z-index: 0;
}

.header {
    grid-column: 1 / span 2;
    padding-bottom: 5px;
}

.header h1 {
    text-align: center;
    color: #f1f1f1;
    font-size: 2.5rem;
    margin-bottom: 5px;
}

hr {
    margin: 20px 0;
    border: solid 2px #bb80ff;
    box-shadow: 0px 0px 10px #bb80ff;
}

.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    row-gap: 20px;
    padding: 30px;
    background-color: #161616;
    border-radius: 10px;
    box-shadow: 0px 0px 10px #060606;
}

.card:hover {
    box-shadow: 0px 5px 10px #bb80ff;
    transition: 0.3s ease-in-out;
}

.card h1 {
    color: #f1f1f1;
    font-size: 2rem;

}
</style>