<<<<<<< HEAD
### 1. 기본라우터 설정 및 다운로드
    "styled-components": "^6.1.12",
    "react-router-dom": "^6.26.0"

### 2. 브라우저 라우터 기본 설정
=======
### 1. 프로젝트 생성및 기본 환경 설정
npm create vite@latest react-hjs-lion-game-project

### 2. 라이브러리 다운로드 후 실행
npm i<br>
npm run dev

### 3. 프리티어 설정
{
"printWidth": 120, // 한 줄의 최대 길이를 120자로 제한
"tabWidth": 2, // 들여쓰기 크기를 2칸으로 설정
"trailingComma": "all", // 모든 곳에서 마지막 요소 뒤에 쉼표 추가
"singleQuote": true, // 문자열에 작은 따옴표(') 사용
"jsxSingleQuote": true, // JSX에서 작은 따옴표(') 사용
"semi": false // 세미콜론을 사용하지 않음
}

### 4. eslint 문법 아래와 같이 수정
    사용하지 않는 변수및 모듈 빨간줄에러를 경고로 처리
    eslint.config.js

    // 'no-unused-vars': ['error', { varsIgnorePattern: '^[A-Z]' }],
    'no-unused-vars': 'warn',

### 5. 부트스트랩 다운로드
    "bootstrap": "^5.3.3"

### 6. 개발위한 기본파일 정리
    index.css 삭제 -> main.jsx에서 import 삭제
    App.css 삭제 -> App.jsx에서 import 삭제


### 7. 패스 앨리어스 설정(@)

####  vite.config.js 설정

```
import path from "path";

export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: [{ find: '@', replacement: path.resolve(__dirname, 'src') }],
  },
})

```

jsonconfig.json => vs code 를 위한 설정(절대 경로 패스를 설정하기 위해 주로 설정)

https://until.blog/@ninefloor/path-alias-with-vite----자동완성-설정-
Path Alias with Vite

jsonconfig.json 파일을 만든후
아래를 추가

```
{
    "compilerOptions": {
    "baseUrl": ".",
    "paths": {
    "@/": ["./src/_"]
    }
    },
    "exclude": ["node_modules"] //프로젝트 규모가 크다면 성능(intellisense)이 낮아질 수 있는데 이 때 내가 실질적으로 사용하지 않는 파일들을 제외해줄 수 있다.
}
```
>>>>>>> 40f49228b88dc2e3c6c8feacb7cebbf3959ee56f
