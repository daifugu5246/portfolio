<script setup lang="ts">

</script>

<template>
    <div class="home" id="home">
        <div class="home-text">
            <h1>Hello, My name is <br><span>Patipat Koeddang</span></h1>
            <hr>
            <h2>Computer Engineering @ KMITL</h2>
            <a href="mailto:patipat.kd@gmail.com" target="_blank"><button class="btn">Hire me<span><font-awesome-icon icon="fa-solid fa-arrow-up-right-from-square" /></span></button></a>
        </div>
        <img class="profile" src="/assets/profile.jpg" alt="Profile Picture" />
    </div>
</template>

<style scoped>
.home {
    display: grid;
    background: linear-gradient(to top, rgba(66, 25, 113, 0.8) 0%, rgba(17, 17, 17, 0.5) 30%);
    grid-template-columns: 1fr 1fr;
    position: relative;
    align-items: center;
    width: 100%;
    height: 100vh;
    padding: 250px 300px 150px 300px;
    z-index: 0;
}

.home-text {
    grid-column: 1;
    margin-right: 20px;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.home-text * {
    color: #f1f1f1;
    text-align: start;
}

.home-text h1{
    font-size: 2.5rem;
    width: 600px;
}

.home-text h1 span{
    font-size: 4rem;
    color: #bb80ff;
}

.home-text hr{
    border : solid 2px;
    box-shadow: 0px 0px 20px #f1f1f1;
}

.home-text h2{
    font-size: 2rem;
}

.profile {
    grid-column: 2;
    justify-self: end;
    width: 350px;
    border-radius: 50%;
    box-shadow: 0px 0px 40px #8e44e2;
}

.btn {
    width: 150px;
    height: 50px;
    margin-top: 20px;
    padding: 10px 5px;
    text-align: center;
    font-size: 1.2rem;
    font-weight: 600;
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
    margin-left: 5px;
}

.btn:hover {
    box-shadow: 0px 0px 20px #8e44e2;
    transition: 0.3s;
}

@media (max-width: 1600px) {
    .home{
        padding: 150px 200px 
    }
    .home h1 {
        width: 100%;
        font-size: 2rem;
    }
    .home h1 span {
        font-size: 3.5rem;
    }
    .home-text h2{
        font-size: 2rem;
    }
    .profile{
        width: 300px;
    }
}

@media (max-width: 1440px) {
    .home{
        padding: 150px 200px 
    }
    .home h1 {
        width: 100%;
        font-size: 1.5rem;
    }
    .home h1 span {
        font-size: 3rem;
    }
    .home-text h2{
        font-size: 1.5rem;
    }
    .profile{
        width: 280px;
    }
}

@media (max-width: 1024px) {
    .home{
        display: grid;
        grid-template-columns: 1fr;
        row-gap: 30px;
        padding: 150px;
    }
    .home-text{
        grid-column: 1;
        grid-row: 2;
        margin: 0;
    }
    .home-text * {
        text-align: center;
    }
    .home h1 {
        width: 100%;
        font-size: 2.3rem;
    }
    .home h1 span {
        font-size: 3.5rem;
    }
    .home-text h2{
        font-size: 1.8rem;
    }
    .profile{
        grid-column: 1;
        grid-row: 1;
        justify-self: center;
        width: 300px;
    }
}

@media (max-width: 600px) {
    .home{
        padding: 150px 50px 150px 50px;
    }
    .home h1 {
        width: 100%;
        font-size: 1.5rem;
    }
    .home h1 span {
        font-size: 2.5rem;
    }
    .home-text h2{
        font-size: 1.5rem;
    }
    .profile{
        width: 200px;
    }
}
</style>