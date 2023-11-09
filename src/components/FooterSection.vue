<script setup>
import { footerText } from "@/constants/index"
</script>
<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>JeongUZIN</div>
                <div>@uzins</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li v-for="(foot, key) in footerText">
                            <a :href=foot.link>{{ foot.title }}</a>
                            <em>{{ foot.desc }}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 JeongUZIN<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
.footer__inner {
    padding: 16px;
}


.footer__text {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 5px 0;
    border-top: 1px solid;
    border-bottom: 1px solid;
}

.footer__text div {
    font-size: 0.7vw;
}

.footer__info {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: stretch;
    margin: 3rem 0;
}

.footer__info>div {
    width: 50%;
}

.footer__info>div.left {
    width: 40%;
}

.footer__inner .footer__info .left .title {
    background: url(../assets/img/go.svg) no-repeat right 17px;
    border-bottom: 1px solid var(--mainBg-color);
    border-bottom: 1px solid var(--black);
    border-top: 2px solid var(--mainBg-color);
    border-top: 2px solid var(--black);
    font-weight: 700;
    padding: 20px 0;
    text-transform: uppercase;
    transition: all .3s;
}

.footer__inner .footer__info .left .desc {
    margin-top: 10px;
    font-size: 13px;
}

.footer__info .right ul li {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
    border-bottom: 1px solid;
}

.footer__info .right h3 {
    font-weight: 700;
    border-bottom: 1px solid;
    padding: 20px 0;
    border-top: 2px solid;
}

.footer__right {
    background: #262626;
    color: #fff;
    text-align: center;
    padding: 2rem;
    font-size: 0.7vw;
    line-height: 1.5;
}
</style>