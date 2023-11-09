<script setup>
import { portText } from '@/constants/index';
</script>


<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                Portfolio <em>포폴 작업물</em>
            </div>
            <div class="port__wrap">
                <div v-for="(port, key) in portText" :key="key" :class="['port__item', 'p' + (key + 1)]">
                    <span class="num">{{ port.num }}</span>
                    <a href="#">
                        <img :src=port.img :alt=port.title>
                    </a>
                    <h3 class="title">{{ port.title }}</h3>
                    <p class="desc">{{ port.desc }}</p>
                    <a class="port__btn" :href=port.view>사이트 보기</a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: false,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>


<style lang="scss">
#port {
    margin-top: 30vh;
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
    margin-top: 5rem;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
    padding-top: 20px;
}

.port__item {
    width: 500px;
    height: 70vh;
    background-color: var(--subBg300);
    margin-right: 20px;
    padding: 1.5rem 2.5rem;
    color: var(--mainBg-color);
}

.port__item:nth-child(2n) {
    background: #dcf2ff;
}

.port__item span.num {
    font-size: 2.5rem;
    font-weight: 700;
    color: var(--mainfont-color);
}

.port__item a {
    display: block;
    border-radius: 0;
    overflow: hidden;
    margin-top: -15px;
    transition: all 0.3s;
    filter: grayscale(1);
}

.port__item a:hover {
    margin-top: 0;
    filter: grayscale(0);
    border-radius: 20px;
}

.port__item h3 {
    font-size: 1.4rem;
    font-weight: 600;
    text-align: center;
    padding: 12px 0;
    border-bottom: 2px dotted var(--mainBg-color);
    margin-bottom: 12px;
}

.port__item p.desc {
    line-height: 1.4;
}

.port__item a.port__btn {
    width: 100%;
    text-align: center;
    padding: 12px;
    border: 1px solid;
    border-radius: 0;
    margin-top: 20px;
}

.port__title {
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


.port__title em {
    font-family: var(--mainKor-font);
    font-size: 1.5rem;
    font-weight: 700;
}

@media (max-width:800px) {

    .port__title {
        width: 100%;
        margin-bottom: 10vw;
        background-color: var(--mainBg-color);
        font-size: 9vw;
        top: 70px;
        padding: 0.5rem 0;
    }
}
</style>