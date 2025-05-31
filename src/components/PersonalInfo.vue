<script setup lang="ts">

</script>

<template>
    <div class="about-me" id="about-me">
        <div class="story">
            <h1>About me</h1>
            <hr>
            <p>
                Hello, I'm Patipat Koeddang, I graduated from computer engineering at KMITL recently. I have a passion for software development and artificial intelligence. I always enjoy learning new technologies. I have experience in web development and LLM development for financial article writing. I am always eager to learn and improve my skills.
            </p>
        </div>
        <div class="education">
            <h1>Education</h1>
            <hr>
            <ul>
                <li class="edu-li">
                    <img class="kmitl-logo" src="/assets/kmitl.png" alt="KMITL Logo" />
                    <div>
                        <h3>King Mongkut's Institute of Technology Ladkrabang</h3>
                        <p>Computer Engineering</p>
                        <p>2021-2024</p>
                        <p>GPA: 3.34 (Secondary Class Honor)</p>
                    </div>
                </li>
                <li class="edu-li">
                    <img class="ayw-logo" src="/assets/ayw.png" alt="High School Logo" />
                    <div>
                        <h3>Ayutthaya Wittayalai School</h3>
                        <p>Science-Math Program</p>
                        <p>2018-2020</p>
                        <p>GPA: 3.80</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.about-me {
    display: grid;
    position: relative;
    grid-template-columns: 1fr 1fr;
    column-gap: 30px;
    width: 100%;
    height: fit-content;
    padding: 150px 300px 150px 300px;
    z-index: 0;
}

.story {
    grid-column: 1;
}

.story h1 {
    text-align: center;
    color: #f1f1f1;
    font-size: 2.5rem;
    margin-bottom: 5px;
}

hr {
    border: solid 2px #bb80ff;
    margin: 20px 0;
    box-shadow: 0px 0px 10px #bb80ff;
}

.story p {
    color: #f1f1f1;
    font-size: 1.5rem;
    text-align: start;
    line-height: 2.7rem;
}

.education h1 {
    text-align: center;
    color: #f1f1f1;
    font-size: 2.5rem;
    margin-bottom: 5px;
}

.education ul {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    list-style: none;
    letter-spacing: 1px;
    line-height: 2rem;
    color: #f1f1f1;
}

.education {
    grid-column: 2;
}

.edu-li {
    display: flex;;
    align-items: center;
    gap: 20px;
    background: #161616;
    width: 100%;
    padding: 30px;
    color: #f1f1f1;
    border-radius: 10px;
    box-shadow: 0px 0px 10px #060606;
    line-height: 2rem;
}

.edu-li:hover {
    box-shadow: 0px 5px 10px #bb80ff;
    transition: 0.3s ease-in-out;
}

.edu-li h3 {
    color: #f1f1f1;
    font-size: 1.3rem;
}

.edu-li p {
    color: #a6a6a6;
    font-size: 1.1rem;
}

.kmitl-logo {
    width: 120px;
    height: 120px;   
}

.ayw-logo {
    position: relative;
    width: 120px;
    height: 120px;
}

@media (max-width: 1600px) {
    .about-me{
        padding: 100px 150px 150px 150px;
    }
}

@media (max-width: 1440px) {

}

@media (max-width: 1024px) {
    .about-me{
        grid-template-columns: 1fr;
        row-gap: 20px;
    }
    .story {
        grid-column: 1;
    }
    .story p{
        text-align: center;
    }
    .education {
        grid-column: 1;
    }
}

@media (max-width: 600px) {
    .about-me{
        padding: 30px 50px 150px 50px;
    }

    .story h1 {
        font-size: 2.2rem;
    }

    .story p {
        color: #f1f1f1;
        font-size: 1.2rem;
        line-height: 2.7rem;
    }

    .education h1 {
        font-size: 2.2rem;
    }

    .edu-li{
        flex-direction: column;
        text-align: center;
    }
}

</style>