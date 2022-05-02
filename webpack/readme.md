### package 설치

```jsx
yarn init -y
```

### react 설치

```jsx
yarn add react react-dom react-refresh
```

> react-refresh 란? 코드를 수정할 경우 새로고침 하지않고, 수정된 사항을 빠르게 교체해주는 라이브러리이다.


### Babel 설치

```jsx
yarn add @babel/core @babel/preset-env @babel/preset-react
```

> 바벨은 최신 자바스크립트 문법을 구형 브라우저에서도 동작하게 ( === polyfill ), 혹은 리액트의 jsx 문법을 자바스크립트 문법으로 변환해주는 자바스크립트 컴파일러이다.

> @babel/core - 바벨을 이용하기 위해 사용

> @babel/preset-env - 최신 자바스크립트 문법을 구형 브라우저에서도 작동하도록 변환하거나 폴리필 추가

>@babel/preset-react - 리액트의 JSX 문법을 변환

### Babel Config 설정

```jsx
{
  "presets": [
    "@babel/preset-env",
    ["@babel/preset-react", { "runtime": "automatic" }]
  ]
}
```

### webpack 설치

```jsx
yarn add webpack webpack-cli webpack-dev-server
```

> webpack - 직접 작성한 코드나 여러 라이브러리의 자바스크립트 코드를 하나로 묶고 최적화해준다.

>  webpack-cli - 개발자가 맞춤형 웹팩 프로젝트를 설정할 때 속도를 높일 수 있는 유연한 명령 세트를 제공합니다

> webpack-dev-server - 파일이 변화할 때마다 실시간으로 빌드하는 개발 서버 구동


### loader 설치

```jsx
yarn add babel-loader css-loader style-loader
```

> loader는 웹팩이 파일을 빌드할 때 파일을 해석하기 위한 패키지이다.

>babel-loader - jsx 파일과 최신 자바스크립트 문법을 변환(바벨과 연동)

>css-loader - css 파일을 해석

>style-loader - css를 dom에 삽입


### Plugin 설치

```jsx
yarn add html-webpack-plugin mini-css-extract-plugin interpolate-html-plugin @pmmmwh/react-refresh-webpack-plugin
```

> Plugin은 웹팩이 해석한 결과물을 처리하는 패키지이다.

> html-webpack-plugin - html 파일에 번들링 된 js 파일을 삽입

> mini-css-extract-plugin - js 파일과 css 파일을 분리

> interpolate-html-plugin - html 파일에서 %ENV% 같은 템플릿 구문 사용 가능. 꼭 필요한 건 아니지만 CRA 기본 예제 파일에서 %PUBLIC_URL%을 사용하기 때문에 이를 변환하기 위해 설치

> @pmmmwh/react-refresh-webpack-plugin - 좀 더 우수한 핫 리로드 패키지인 react-refresh 사용
