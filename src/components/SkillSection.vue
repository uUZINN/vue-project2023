<script setup>
import { skillText } from "@/constants/index"
</script>

<template>
    <section id="skill">
        <div class="skill__inner">
            <h2 class="skill__title">
                challenge <em>나의 도전</em>
            </h2>
            <div class="skill__desc">
                <div v-for="(skill, key) in skillText" :key="key">
                    <span>{{ key + 1 }}. </span>
                    <h3>{{ skill.text }}</h3>
                    <p>{{ skill.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
}

.skill__title {
    width: 50%;
    font-size: 5vw;
    font-weight: 900;
    text-transform: uppercase;
    font-family: var(--mainEng-font);
    line-height: 1;
    border-bottom: 6px solid var(--mainfont-color);
    position: sticky;
    top: 70px;
    left: 0;
    padding: 10px 0;
}

.skill__title em {
    font-family: var(--mainKor-font);
    font-size: 1.5rem;
    font-weight: 700;
}

.skill__desc {
    width: 48%;
}

.skill__desc div {
    padding-bottom: 20rem;
}

.skill__desc div span {
    font-size: 6rem;
    font-weight: bold;
}

.skill__desc div h3 {
    font-weight: 800;
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
    border-bottom: 1px solid var(--mainfont-color);
    padding-bottom: 10px;
}

.skill__desc div p {
    line-height: 1.7;
    font-size: 1.2rem;
}

@media (max-width:800px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        background-color: var(--mainBg-color);
        font-size: 9vw;
        top: 70px;
        padding: 0.5rem 0;
    }

    .skill__desc {
        width: 100%;
    }

    .skill__desc span {
        font-size: 2vw;
    }
}
</style>