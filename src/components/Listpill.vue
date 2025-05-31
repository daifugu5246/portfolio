<script setup lang="ts">
import { defineProps } from 'vue';
const props = defineProps({
    items: {
        type: Array as () => { name: string; icon: string }[],
        required: true
    },
    justifyContent: {
        type: String
    }
});
</script>
<template>
    <div class="list-pill">
        <ul :style="{'justify-content': props.justifyContent}">
            <li v-for="item in props.items"><img class="icon" :src="item.icon"><p class="icon-text">{{ item.name }}</p></li>
        </ul>
    </div>
</template>
<style scoped>

.icon {
    width: 25px;
    height: 25px;
    margin-right: 10px;
}

.list-pill ul{
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    list-style: none;
    font-size: 1.2rem;
    letter-spacing: 1px;
    line-height: 2rem;
    color: #f1f1f1;
}

.list-pill ul li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #090909;
    padding: 5px 20px;
    border: #bb80ff solid 1px;
    border-radius: 20px;
    box-shadow: 0px 0px 5px #bb80ff;
}

.list-pill ul li:hover {
    text-shadow: #bb80ff 0px 0px 20px;
    transform: scale(1.05);
    transition: 0.3s ease-in-out;
}

@media (max-width: 600px) {
    .icon {
        width: 22px;
        height: 22px;
    }

    .list-pill ul {
        font-size: 1.1rem;
    }
}

@media (max-width: 450px) {
    .icon {
        width: 18px;
        height: 18px;
    }

    .list-pill ul {
        font-size: 1rem;
    }

    .list-pill ul li {
        padding: 3px 8px;
    }
}
</style>