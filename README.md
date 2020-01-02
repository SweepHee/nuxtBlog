# test-blog

> My fabulous Nuxt.js project

## Build Setup

``` bash

yarn create nuxt-app <projectname>

npm install -g firebase-tools
-파이어베이스 전역 설치

yarn add firebase
- 파이어베이스를 디펜던시에 설치함.
- 현재 버전에서 에러나는데 core-js 문제임.
- 패키지.json -> 디펜던시 ->  "core-js": "^2.6.10" 추가 -> yarn
- core-js 다운그래이드 되면서 오류 사라짐.

yarn add nuxt-fire
- $ firebase 명령어 같은거 쓸 수 있음.

= nuxt.config.js의 modules 부분 수정해줌
  modules: [
    '@nuxtjs/axios',
    '@nuxtjs/dotenv',
    [
      'nuxt-fire',
      {
        config: {
   // 이 부분 파이어베이스 프로젝트설정-> SDK snippet 구성에서 가져오면됨.
          apiKey: '',
          authDomain: '',
          databaseURL: '',
          projectId: '',
          storageBucket: '',
          messagingSenderId: '',
          appId: '',
          measurementId: ''
        },
        services: {
          firestore: true
        #   auth: true
        }
      }
    ]
  ],



firebase login
- 파이어베이스 로그인
firebase init
- 파이어베이스 적용
firebase deploy
- 파이어베이스 배포


```



## 파이어베이스 설정

```

파이어베이스 -> 프로젝트 생성
콘솔-> Database 생성
콘솔 -> Project Overview 옆에 톱니바퀴 -> 프로젝트 설정 
-> 지원이메일 잡아줌 -> 앱추가 -> 앱이름 정해주고 나머지 거의 의미 없음. 적당히 맞아보이는거 해주고 넘기기

```


# INSTALLATION

## 파이어베이스 설정파일 루트에 만들 것

**firebaseConfig.js**
```javascript
export default {
      apiKey: 'AIzaSyB7DuJdH3R5jFVrIM5vgzACg3GoXNJjEiY',
      authDomain: 'nuxt-test-77ca3.firebaseapp.com',
      databaseURL: 'https://nuxt-test-77ca3.firebaseio.com',
      projectId: 'nuxt-test-77ca3',
      storageBucket: 'nuxt-test-77ca3.appspot.com',
      messagingSenderId: '691521191195',
      appId: '1:691521191195:web:49dce3e01ea0d65f93a7be',
      measurementId: 'G-FFFCDYM87R'
}
```