# vue를 이용한 포트폴리오 사이트 만들기
![image](https://github.com/uUZINN/vue-project2023/assets/89904583/c54e60b8-c238-4db4-9470-10d5b16ad9f4)

Vue.js는 프론트엔드 웹 개발을 위한 자바스크립트 라이브러리로, 사용자 인터페이스를 만들고 관리하는 데 도움을 주는 도구입니다. Vue는 데이터와 뷰를 연결하여 데이터가 변할 때 자동으로 화면을 업데이트하는 반응형 웹 애플리케이션을 만들 수 있게 해줍니다.

1. 컴포넌트 기반 구조: Vue는 컴포넌트 기반 아키텍처를 사용하며, 각 컴포넌트는 재사용 가능한 UI 요소를 나타냅니다. 이로써 애플리케이션을 모듈화하고 관리하기 용이해집니다.

2. 반응형 데이터 바인딩: Vue에서는 데이터와 화면 요소를 간단히 연결할 수 있습니다. 데이터가 변경되면 자동으로 화면이 업데이트되며, 화면 요소가 변경되면 데이터에 반영됩니다.

3. 디렉티브: Vue 디렉티브를 사용하여 HTML 요소에 특별한 동작을 부여할 수 있습니다. 예를 들어, v-for 디렉티브는 반복문을 처리하고, v-bind는 요소의 속성과 데이터를 연결하는 데 사용됩니다.

4. 이벤트 핸들링: Vue는 이벤트 처리를 간단하게 만들어줍니다. 사용자 입력 또는 컴포넌트 간 통신을 효과적으로 다룰 수 있습니다.

5. 라우팅 및 상태 관리: Vue 라우터와 상태 관리 라이브러리인 Vuex를 사용하여 싱글 페이지 애플리케이션 (SPA)을 개발할 때 라우팅 및 상태 관리를 쉽게 처리할 수 있습니다.

## 셋팅
`npm init vue@latest`<br>
√ Project name: ... vue-project<br>
√ Add TypeScript? ... No<br>
√ Add JSX Support? ... Yes<br>
√ Add Vue Router for Single Page Application development? ... Yes<br>
√ Add an End-to-End Testing Solution? » No<br>
√ Add ESLint for code quality? ... Yes<br>
√ Add Prettier for code formatting? ... Yes<br>
<br>
`cd vue-project`<br>
`npm install`<br>
`npm run format`<br>
`npm run dev`<br>
<br>
gsap 설치 : `npm install gsap`<br>
sass 설치 : `npm install sass`<br>
lenis 설치 : `npm install @studio-freight/lenis`<br>

### vercel
Vercel은 클라우드 기반의 호스팅 및 배포 플랫폼으로, 웹 애플리케이션 및 정적 웹사이트를 쉽게 배포하고 관리할 수 있도록 도와주는 서비스입니다.
<br><br>
[vercel 홈페이지] (https://vercel.com/)<br>
git 아이디 연동 후 프로젝트 생성<br>
https://vue-project2023.vercel.app/

### VIEW CODE
```
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
```

1. data: isNavVisible라는 데이터 속성을 가지고 있습니다. 이 속성은 네비게이션의 가시성을 토글하는 데 사용됩니다. 초기값은 false로 설정되어 있습니다.

2. methods:
   - toggleMobileMenu: 모바일 메뉴를 토글하는 메서드입니다. isNavVisible 값을 반전시켜 메뉴를 열거나 닫습니다.
   - scrollLink: 스크롤 링크를 처리하는 메서드입니다. 이벤트를 받아 해당 링크의 타겟 엘리먼트로 스무스하게 스크롤하는 기능을 수행합니다.
  

```
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
```

mounted() 라이프 사이클 훅에서 scrollAnimation() 메서드를 호출하여, .port__item 클래스를 가진 요소들을 수평으로 이동시키는 애니메이션을 설정합니다. 
ScrollTrigger를 이용하여 페이지의 스크롤 위치에 따라 트리거되며, 특정 요소를 스크롤에 고정시키고 애니메이션을 부드럽게 만들어줍니다.
