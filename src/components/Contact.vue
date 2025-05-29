<script setup lang="ts">
import { ref } from 'vue';

const resumeUrl = ref('https://drive.google.com/file/d/1NvAheLr-x5bGXaFTLffEduTEaPvX_wug/view?usp=drive_link');
const gradeUrl = ref('https://drive.google.com/file/d/1hcAhMdRAlJpBnKLubs5DJgtiB26BYRus/view?usp=drive_link');
</script>

<template>
    <div class="contact" id="contact">
        <h1>Contact</h1>
        <hr>
        <div class = "contact-container">
            <a class="contact-text" href="mailto:patipat.kd@gmail.com"><span><font-awesome-icon icon="fa-solid fa-envelope" /></span>patipat.kd@gmail.com</a><br>
            <a class="contact-text"  href="tel:+66900135630"><span><font-awesome-icon icon="fa-solid fa-phone" /></span>0900135630</a>
            <p class="contact-text"><span><font-awesome-icon icon="fa-solid fa-location-dot" /></span>6 village 4 Koh Kerd Bang Pa-in Ayutthaya 13160</p>
            <div class="btn-container">
                <a :href="resumeUrl" target="_blank"><button class="btn"><span><font-awesome-icon icon="fa-solid fa-download" /></span>My Resume</button></a>
                <a :href="gradeUrl" target="_blank"><button class="btn"><span><font-awesome-icon icon="fa-solid fa-download" /></span>Transcript</button></a>
            </div>
        </div>
    </div>
    <footer class="footer">
        <p>© 2025 Patipat Koeddang. All rights reserved.</p>
    </footer>
</template>

<style scoped>
.contact {
    width: 100%;
    height: fit-content;
    padding: 150px 250px 50px 250px;
    z-index: 0;
}

.contact h1 {
    color: #f1f1f1;
    font-size: 2.5rem;
    margin-bottom: 5px;
    text-align: center;
}
.contact hr {
    border: solid 2px #bb80ff;
    margin: 20px 0px 50px 0px;
    box-shadow: 0px 0px 10px #bb80ff;
}

.contact-container {
    text-align: center;
    text-decoration: none;
    color: #f1f1f1;
    font-size: 1.5rem;
    border-radius: 10px;
    line-height: 2.3rem;
}

.contact-text {
    text-decoration: none;
}

.contact-text span {
    margin-right: 10px;
    color: #bb80ff;
}

.btn-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 50px;
}

.btn {
    width: fit-content;
    height: fit-content;
    padding: 15px 20px; 
    text-align: center;
    font-size: 1.2rem;
    font-weight: 600;
    text-decoration: none;
    color: #f1f1f1;
    background-color: #8e44e2;
    border: none;
    border-radius: 10px;
    cursor: pointer;
}

.btn span {
    display: inline-block;
    position: relative;
    top: 1px;
    color: #f1f1f1;
    font-size: 1.2rem;
    margin-right: 5px;
}

.btn:hover {
    box-shadow: 0px 0px 20px #8e44e2;
    transition: 0.3s;
}

.footer {
    width: 100%;
    height: fit-content;
    padding: 5px 0;
    background-color: #060606;
    color: #f1f1f1;
    text-align: center;
    font-size: 0.8rem;
}
</style>