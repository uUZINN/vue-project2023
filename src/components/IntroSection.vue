<template>
    <section id="intro">
        <div class="intro__inner">
            <h1 class="intro__title">
                UZIN Developer
            </h1>
            <div class="intro__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="intro__text">
                <div class="text">
                    <div>where there</div>
                    <div>is a will there is</div>
                    <div>a way</div>
                </div>
                <div class="img">

                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
body {
    background-color: var(--mainBg-color);
}

#intro {
    height: 110vh;
}

.intro__inner {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    flex-direction: column;
    background-color: var(--mainBg-color);
    padding: 1vw;
}

.intro__title {

    font-size: 10.5vw;
    text-transform: uppercase;
    font-weight: bold;
    font-family: 'Russo One', sans-serif;
    line-height: 1;
    color: var(--mainfont-color);
}

.intro__lines {
    display: block;
    width: 100%;
}

.intro__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--subBg300);
    margin-bottom: 0.5vw;
}

.intro__lines .line:nth-child(1) {
    height: 1px;
}

.intro__lines .line:nth-child(2) {
    height: 2px;
}

.intro__lines .line:nth-child(3) {
    height: 3px;
}

.intro__lines .line:nth-child(4) {
    height: 4px;
}

.intro__lines .line:nth-child(5) {
    height: 5px;
}

.intro__lines .line:nth-child(6) {
    height: 6px;
}

.intro__lines .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom .line:nth-child(1) {
    height: 1px;
}

.intro__lines.bottom .line:nth-child(2) {
    height: 2px;
}

.intro__lines.bottom .line:nth-child(3) {
    height: 3px;
}

.intro__lines.bottom .line:nth-child(4) {
    height: 4px;
}

.intro__lines.bottom .line:nth-child(5) {
    height: 5px;
}

.intro__lines.bottom.line:nth-child(6) {
    height: 6px;
}

.intro__lines.bottom .line:nth-child(7) {
    height: 7px;
}

.intro__lines.bottom {
    display: none;
}

.intro__text {
    background-color: var(--subBg300);
    /* height: 37vh; */
    padding: 10vw 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--mainfont-color);
    text-align: center;
    line-height: 1.4;
    position: relative;
}

.intro__text .text {
    font-size: 3.1vw;
    line-height: 1.5;
    text-transform: uppercase;
    font-weight: 900;
    font-family: var(--mainEng-font);
    text-decoration: underline;
    letter-spacing: -0.1vw;
    z-index: 1000;
}

.intro__text .img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 15vw;
    height: 15vw;
    background-image: url(../assets/img/flower.jpg);
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    /* margin: 3rem; */
}

.intro__text .img::after {
    content: '';
    /* background-color: #fff; */
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 30vh;
    height: 30vh;
    background-image: url(../assets/img/face.jpg);
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    /* cursor: pointer; */
}

@media(max-width: 800px) {
    .intro__inner {
        align-items: center;
        justify-content: center;
    }

    .intro__lines.bottom {
        display: block;
    }

    .intro__text .text {
        font-size: 30px;
    }

    .intro__text img {
        width: 300px;
        height: 300px;
    }

    .intro__text img::after {
        opacity: 0.3;
    }
}
</style>