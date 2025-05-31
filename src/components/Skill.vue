<script setup lang="ts">
import { ref } from 'vue';
import ListPill from './Listpill.vue';

const base = ref(import.meta.env.BASE_URL)

const languages = ref([
    { name: 'Python', icon: base.value + '/assets/languages/python.png' },
    { name: 'JavaScript', icon: base.value + '/assets/languages/js.png' },
    { name: 'TypeScript', icon: base.value + '/assets/languages/typescript.png' },
    { name: 'PHP', icon: base.value + '/assets/languages/php.png' },
    { name: 'C#', icon: base.value + '/assets/languages/c-sharp.png' },
    { name: 'C/C++', icon: base.value + '/assets/languages/cpp.png' },
    { name: 'Java', icon: base.value + '/assets/languages/java.png' }
]);

const tools = ref([
    { name: 'React', icon: base.value + '/assets/tools/react.png' },
    { name: 'Vue.js', icon: base.value + '/assets/tools/vue.svg' },
    { name: 'Bootstrap', icon: base.value + '/assets/tools/bootstrap.png' },
    { name: 'Laravel', icon: base.value + '/assets/tools/laravel.png' },
    { name: 'Express.js', icon: base.value + '/assets/tools/expressjs.png' },
    { name: 'MongoDB', icon: base.value + '/assets/tools/mongodb.svg' },
    { name: 'MySQL', icon: base.value + '/assets/tools/mysql.png' },
    { name: 'Git', icon: base.value + '/assets/tools/git.png' },
    { name: 'Postman', icon: base.value + '/assets/tools/postman.svg' },
    { name: 'Docker', icon: base.value + '/assets/tools/docker.png' }
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
            <ListPill :items="languages" justifyContent="center"/>
        </div>
        <div class="tools card"> 
            <h1>Tools & Framework</h1>
            <ListPill :items="tools" justifyContent="center"/>
        </div>
    </div>
</template>

<style scoped>
.skill {
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 20px;
    width: 100%;
    height: fit-content;
    padding: 30px 300px 150px 300px;
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

@media (max-width: 1600px) {
    .skill{
        padding: 30px 150px 150px 150px;
    }
}

@media (max-width: 1440px) {

}

@media (max-width: 1024px) {
    .skill{
        grid-template-columns: 1fr;
        column-gap: 0px;
        row-gap: 20px;
    }
    .languages{
        grid-column: 1;
    }

    .tools{
        grid-column: 1;
    }
}

@media (max-width: 600px) {
    .skill{
        padding: 30px 50px 150px 50px;
    }

    .header h1{
        font-size: 2.2rem;
    }

    .card h1{
        font-size: 1.8rem;
    }
}

@media (max-width: 450px) {
   .skill{
        padding: 30px 20px 100px 20px;
    }

    .header h1{
        font-size: 2rem;
    }

    .card h1{
        font-size: 1.5rem;
    } 
}
</style>