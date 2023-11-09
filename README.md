# vue를 이용한 포트폴리오 사이트 만들기
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
[vercel 홈페이지] (https://vercel.com/)
git 아이디 연동 후 프로젝트 생성
https://vue-project2023.vercel.app/
