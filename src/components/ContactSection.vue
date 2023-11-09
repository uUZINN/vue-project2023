<template>
    <section id="contact">
        <div class="contact__inner">
            <h2 class="contact__title">Contact</h2>

            <div class="contact__line top" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="contact__text">
                <div class="text">
                    <div>
                        <a href="#">KAKAO : dbwls90388141</a>
                    </div>
                    <div>
                        <a href="#">MAIL : dbwls9038@naver.com</a>
                    </div>
                </div>
            </div>
            <div class="contact__line bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
#contact {
    height: 100vh;
}

.contact__title {
    width: 100%;
    font-size: 5vw;
    font-weight: 900;
    text-transform: uppercase;
    font-family: var(--mainEng-font);
    line-height: 1;
    /* border-bottom: 6px solid #000; */
    /* background-color: var(--mainBg-color); */
}

.contact__line {
    margin-top: 2rem;
}

.contact__line .line {
    display: block;
    width: 100%;
    background-color: var(--subBg300);
    margin-bottom: 0.5vw;
}

.contact__line .line:nth-child(1) {
    height: 1px;
}

.contact__line .line:nth-child(2) {
    height: 2px;
}

.contact__line .line:nth-child(3) {
    height: 3px;
}

.contact__line .line:nth-child(4) {
    height: 4px;
}

.contact__line .line:nth-child(5) {
    height: 5px;
}

.contact__line .line:nth-child(6) {
    height: 6px;
}

.contact__line .line:nth-child(7) {
    height: 7px;
}

.contact__line.bottom .line:nth-child(1) {
    height: 7px;
}

.contact__line.bottom .line:nth-child(2) {
    height: 6px;
}

.contact__line.bottom .line:nth-child(3) {
    height: 5px;
}

.contact__line.bottom .line:nth-child(4) {
    height: 4px;
}

.contact__line.bottom .line:nth-child(5) {
    height: 3px;
}

.contact__line.bottom .line:nth-child(6) {
    height: 2px;
}

.contact__line.bottom .line:nth-child(7) {
    height: 1px;
}

.contact__line.top {
    display: none;
}

.contact__line.bottom {
    margin-top: 0;
    margin-top: 0.5vw;
}

.contact__text {
    height: 100%;
    background: var(--subBg300);
    color: var(--mainBg-color);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10vw 0;
    margin-top: 1rem;
}

.text div a {
    font-size: 4vw;
    font-weight: 500;
    font-family: 'Russo One';
    text-decoration: underline;
}

.text div {
    text-align: center;
}

@media (max-width:800px) {

    .contact__title {
        width: 100%;
        margin-bottom: 10vw;
        background-color: var(--mainBg-color);
        font-size: 9vw;
        top: 70px;
        padding: 0.5rem 0;
    }
}
</style>