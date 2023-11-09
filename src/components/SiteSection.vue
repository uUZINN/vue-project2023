<script setup>
import { siteText } from '@/constants/index';
</script>

<template>
    <section id="site">
        <div class="site__inner">
            <div class="site__title">
                Site Coding <em>나의 작업물</em>
            </div>
            <div class="site__wrap">
                <div v-for="(site, key) in siteText" :key="key" :class="['site__item', 's' + (key + 1)]">
                    <span class="num">{{ key + 1 }}. </span>
                    <div class="text">
                        <div>{{ site.text[0] }}</div>
                        <div>{{ site.text[1] }}</div>
                        <div>{{ site.text[2] }}</div>
                    </div>
                    <h3 class="title">
                        {{ site.title }}
                    </h3>
                    <div class="btn">
                        <a :href=site.code>code</a>
                        <a :href=site.view>view</a>
                    </div>
                    <div class="info">
                        <span>{{ site.info[0] }}</span>
                        <span>{{ site.info[1] }}</span>
                        <span>{{ site.info[2] }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.site__inner {
    padding: 16px;

}

.site__title {
    width: 100%;
    font-size: 5vw;
    font-weight: 900;
    text-transform: uppercase;
    font-family: var(--mainEng-font);
    line-height: 1;
    border-bottom: 6px solid var(--mainfont-color);
    position: sticky;
    top: 70px;
    left: 0;
}


.site__title em {
    font-family: var(--mainKor-font);
    font-size: 1.5rem;
    font-weight: 700;
}

.site__wrap {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.site__wrap .site__item {
    width: 100%;
    background: #0000008a;
    border-radius: 20px;
    margin-top: 1rem;
    padding: 4rem;
    color: var(--black);
    text-align: center;
    position: sticky;
    left: 0;
}

.site__item.s1 {
    top: 180px;
    background: var(--subBg300);
}

.site__item.s2 {
    top: 200px;
    background: #d8f9eb;
}

.site__item.s3 {
    top: 220px;
    background: #d8f1f9;
}

.site__item.s4 {
    top: 240px;
    background: #d8e2f9;
}

.site__wrap .site__item .title {
    font-size: 1.8rem;
    font-weight: 700;
    position: sticky;
    left: 0;
    top: 0;
}

.site__wrap .site__item .btn {
    margin: 1.5rem 0 2.5rem;
}

.site__wrap .site__item .info {
    line-height: 1.5;
}

.site__wrap .site__item .info span {
    display: block;
}

.site__wrap .site__item .btn a {
    display: inline-block;
    padding: 0.7rem 2.5rem;
    border-radius: 50px;
    border: 1px solid #000;
    margin: 0 0.3rem;
    font-weight: 600;
}

.site__item span.num {
    font-size: 4.5vw;
    font-weight: bold;
    color: var(--black);
    text-align: left;
    display: inline-block;
    position: absolute;
    left: 4rem;
    top: 3rem;
}

.site__item .text {
    margin-bottom: 3rem;
}

.site__item .text div {
    font-weight: 600;
    font-size: 3.5vw;
    line-height: 1.5;
    text-align: center;
    text-transform: capitalize;
    font-family: 'Russo One', sans-serif;
}

@media (max-width:800px) {

    .site__title {
        width: 100%;
        margin-bottom: 10vw;
        background-color: var(--mainBg-color);
        font-size: 9vw;
        top: 70px;
        padding: 0.5rem 0;
    }

    .site__item .text div {
        font-size: 6vw;
    }
}
</style>