<script setup lang="ts">
import Card from './Card.vue';
import { ref } from 'vue';

const base = ref(import.meta.env.BASE_URL)

const experience = ref([
    {
        title: 'Full Stack Developer (Intern)',
        subtitle: 'Dataxet Limited',
        duration: 'April 2024 - June 2024',
        descriptions: [
            "Developed internal website integrating web scraping APIs for social media data extraction and CSV conversion",
            "Designed responsive user interface",
            "Designed SQL database architecture",
            "Implemented queueing functions, scheduler and email notification system",
            "Collaborated with DevOps teams for production deployment"
        ],
        tools: [{ name: 'Vue.js', icon: base.value + '/assets/tools/vue.svg' }, { name: 'Laravel', icon: base.value + '/assets/tools/laravel.png' }, { name: 'MySQL', icon: base.value + '/assets/tools/mysql.png' }],
    },
    {
        title: 'Financial Article Writing using Artificial Intelligence',
        subtitle: 'Thesis',
        duration: 'December 2023 - March 2024',
        descriptions: [
            "Researched on LLM methodologies for financial article writing expertise and experimented with fine-tuning approaches",
            "Used Pandas for data manipulation and preprocessing",
            "Implemented model training using Hugging Face Transformers library",
            "Evaluated performance of each fine-tuning method to identify optimal configurations"
        ],
        tools: [{ name: 'Huggingface', icon: base.value + '/assets/tools/huggingface.png' }, { name: 'Pandas', icon: base.value + '/assets/tools/pandas.png' }],
    },
    {
        title: 'Masterpeach',
        subtitle: 'Educational Project',
        duration: 'August 2023 - October 2023',
        descriptions: [
            "Masterpeach, a digital art exchange and auction website with comprehensive API development",
            "Designed and developed API architecture including auctioning and purchasing functions",
            "Created MongoDB database structure",
            "Conducted API testing using Postman",
            "Provided front-end developer support during integration testing"
        ],
        tools: [{ name: 'Express.js', icon: base.value + '/assets/tools/expressjs.png' }, { name: 'MongoDB', icon: base.value + '/assets/tools/mongodb.svg' }],
        code: 'https://github.com/daifugu5246/masterpeach',
    },
    {
        title: 'Todo List',
        subtitle: 'Freetime Project',
        descriptions: [
            "Todo List application with create, update, delete, and status management features",
            "Built user-friendly interface using React and Bootstrap",
            "Implemented task prioritization (important) and completion tracking",
            "Stored data in browser's local storage"
        ],
        tools: [{ name: 'React', icon: base.value + '/assets/tools/react.png' }, { name: 'Bootstrap', icon: base.value + '/assets/tools/bootstrap.png' }],
        demo: 'https://daifugu5246.github.io/to-do-app/',
        code: 'https://github.com/daifugu5246/to-do-app',
    },
    {
        title: 'FeelFood',
        subtitle: 'Educational Project',
        duration: 'April 2023',
        descriptions: [
            "Feelfood, a website enabling users to request friends to buy canteen food",
            "Designed controllers to efficiently return data to views using ASP.NET Core MVC",
            "Implemented database models using Entity Framework as ORM solution",
            "Built complete system with MS SQL Server as database"
        ],
        tools: [{ name: 'ASP.NET Core', icon: base.value + '/assets/tools/asp.png' }, { name: 'MS SQL', icon: base.value + '/assets/tools/mssql.png' }],
        code: 'https://github.com/daifugu5246/feelfood',
    },
]);
</script>

<template>
    <div class="exp" id="exp">
        <h1>Experience</h1>
        <hr>
        <div class="cards">
            <Card v-for="(exp, index) in experience" :key="index" :title="exp.title" :subtitle="exp.subtitle" :duration="exp.duration" :descriptions="exp.descriptions" :tools="exp.tools" :demo="exp.demo" :code="exp.code"/>
        </div>
    </div>
</template>

<style scoped>
.exp {
    width: 100%;
    height: fit-content;
    padding: 30px 300px 150px 300px;
    z-index: 0;
}

hr {
    border: solid 2px #bb80ff;
    margin: 20px 0px;
    box-shadow: 0px 0px 10px #bb80ff;
}

.exp h1 {
    text-align: center;
    color: #f1f1f1;
    font-size: 3rem;
    margin-bottom: 5px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(2, minmax(auto, 1fr));
    gap: 20px;
}

@media (max-width: 1600px) {
    .exp{
        padding: 30px 150px 150px 150px;
        grid-template-columns: 1fr;
        column-gap: 0px;
        row-gap: 20px;
    }
}

@media (max-width: 1440px) {

}

@media (max-width: 1024px) {
    .cards{
        grid-template-columns: repeat(1, minmax(auto, 1fr));
    }
    .languages{
        grid-column: 1;
    }

    .tools{
        grid-column: 1;
    }
}

@media (max-width: 600px) {
    .exp {
        padding: 30px 50px 150px 50px;
    }

    .exp h1 {
        font-size: 2.2rem;
    }
}

@media (max-width: 450px) {
    .exp {
        padding: 30px 20px 100px 20px;
    }

    .exp h1 {
        font-size: 2rem;
    }
}
</style>