<script setup lang="ts">

</script>

<template>
    <nav class="navbar">
        <ul class="navbar-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about-me">About me</a></li>
            <li><a href="#skill">Skills</a></li>
            <li><a href="#exp">Experience</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</template>

<style scoped>
.navbar {
    position: fixed;
    background: linear-gradient(to bottom, #060606 60%, transparent);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1rem 2rem;
    width: 100%;
    height: 150px;
    z-index: 1;
}


.navbar-links {
    background: #060606;
    list-style: none;
    display: flex;
    gap: 2rem;
    margin: 0;
    padding: 0;
}

.navbar-links a {
    background: #060606;
    padding: 5px 0px 5px 0px;
    font-size: 1.5rem;
    text-decoration: none;
}

.navbar-links a:hover {
    color: #bb80ff;
    text-shadow: #f1f1f1 0px 0px 20px;
    font-size: 1.6rem;
    transition: font-size 0.5s, color 0.3s;
}
</style>