<script setup>
import { headerNav } from "@/constants/index"
</script>

<template>
    <header id="header" role="banner">
        <div class="header__inner">
            <div class="header__logo">
                <a href="#">PORTFOLIO <em>by UZIN</em></a>
            </div>
            <nav class="header__nav" role="navigation" aria-label="메인 메뉴" :class="{ show: isNavVisible }">
                <ul>
                    <li v-for="(nav, key) in headerNav" :key="key">
                        <a :href=nav.url @click="scrollLink($event)">{{ nav.title }}</a>
                    </li>
                </ul>
            </nav>
            <div class="header_nav__mobile" id="headerToggle" aria-controls="primary-menu"
                aria-expanded="isNavVisible.toString()" role="button" @click="toggleMobileMenu">

                <span></span>
            </div>
        </div>
    </header>
    <!-- //header -->
</template>

<script>
export default {
    data() {
        return {
            isNavVisible: false,
        };
    },
    methods: {
        toggleMobileMenu() {
            this.isNavVisible = !this.isNavVisible;
        },
        scrollLink(event) {
            event.preventDefault();

            const targetId = event.target.getAttribute("href");
            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                targetElement.scrollIntoView({ behavior: "smooth" });
            }
        },
    },
};
</script>

<style lang="scss">
#header {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    z-index: 10000;
}

.header__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: rgba(0, 0, 0, 0.3);
    padding: 1rem;
    color: var(--subBg100);
    height: 70px;
}

.header__logo {
    width: 40%;
    font-size: 1.5rem;
    font-weight: 800;
    font-family: var(--mainEng-font);
    box-sizing: border-box;
}

.header__logo a {
    font-size: 1.7rem;
    font-weight: 600;
}

.header__logo a em {
    font-size: 0.8rem;
    font-weight: 200;
}

.header__logo a:hover {
    color: var(--white);
}

.header__nav {
    width: 60%;
}


.header__nav ul {
    display: flex;
    justify-content: right;
}


.header__nav li {
    display: inline;
    padding: 0.3vh 1.8vw;
}

.header__nav ul li a {
    text-transform: uppercase;
    font-family: var(--mainEng-font);
    font-weight: 500;
    font-size: 1.3rem;
    position: relative;
}

.header__nav ul li a::before {
    content: '';
    width: 100%;
    height: 1px;
    background-color: var(--subBg200);
    position: absolute;
    left: 0;
    bottom: 0;
    transform: scaleX(0);
    transition: all 0.3s;
}

.header__nav ul li a:hover::before {
    transform: scaleX(1);
    color: var(--white);
}

.header__nav ul li a:hover {
    color: var(--white);
}

.header_nav__mobile {
    width: 40px;
    height: 40px;
    cursor: pointer;
    display: none;
}

.header_nav__mobile span {
    display: block;
    width: 40px;
    height: 2px;
    background-color: var(--subBg100);
    margin-top: 19px;
    position: relative;
}

.header_nav__mobile span::before {
    content: '';
    width: 40px;
    height: 2px;
    background-color: var(--subBg100);
    position: absolute;
    right: 0;
    top: 6px;
    transition: width 0.3s;
}

.header_nav__mobile span::after {
    content: '';
    width: 40px;
    height: 2px;
    background-color: var(--subBg100);
    position: absolute;
    left: 0;
    bottom: 6px;
    transition: width 0.3s;
}

@media (max-width: 800px) {
    .header__logo {
        width: 50%;
    }

    .header__nav {
        display: none;
    }

    .header__nav.show {
        display: block;
    }

    .header__nav.show ul {
        display: block;
        position: absolute;
        right: 0;
        top: 70px;
        background-color: var(--subBg400);
        z-index: 1000;
        min-width: 159px;
        padding: 20px 0;
    }

    .header__nav.show li {
        display: block;
        text-align: right;
    }

    .header__nav.show li a {
        display: inline-block;
        padding: 10px;
    }

    .header__nav.show+.header_nav__mobile span::before {
        width: 20px;
    }

    .header__nav.show+.header_nav__mobile span::after {
        width: 20px;
    }

    .header_nav__mobile {
        display: block;
    }
}
</style>