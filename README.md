# TIL

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2a957f8-ea60-407b-90f7-87e5642360c8/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/38b4d6fc-d161-477e-a949-f4d9d65a6726/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b0f2b06a-88b1-44cb-98ae-e17020be1732/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/326fc646-410a-4819-9189-a8861cc00eae/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0af1197d-1db4-4e22-909f-031f001a2c9a/Untitled.png)

create-react-app으로 간단히 바벨과 웹팩 설정 자동 가능

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9c1ae46d-861a-495b-866e-eb872ee7f88c/Untitled.png)

웹팩- 번들시켜주는 역할

npx create-react-app 원하는 디렉토리 안에 리액트 설치

npm은 레지스트리 저장소의 역할

레지스트리-디펜던시 저장

빌드해서 배포시 빌드할 때도 npm 사용

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/862c9a4c-88b6-4e77-ac1f-3eb477a896e8/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a012929c-f129-44a8-9ac8-9fdabdda1dfc/Untitled.png)

예전엔 글로벌로 다운받았으나 npx의 등장으로 이제 다운 없이도 사용 가능하다.

app.js가 첫 페이지

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ca3f92c5-16f0-48d4-9e3f-085b2ebd846b/Untitled.png)

index.js에서 index.html의 root 부분에 보여줄 내용이 app.js임을 설정

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/aacdcb6c-5e6c-4107-b224-6287919c65e5/Untitled.png)

웹팩은 src안에서 관리

src안에 이미지 넣어줘야 웹팩이 관리해줄 수 있다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8f608d70-eae9-4f0a-bedf-f2c2d4cd4253/Untitled.png)

**HOC** 는 다른 컴포넌트를 갖는 function, 자격을 확인하거나 다른 기능으로

다른 많은 컴포넌트가 기능을 이용할 수 있게

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42605d57-fbbc-42bd-84df-33e60f7126e5/Untitled.png)

**CORS 에러 해결 위한 proxy 설정**

클라이언트단에서

npm install http-proxy-middleware —save

**프엔 백엔 서버 한번에 켜기 위한 디펜던시**

npm install concurrently --save

**리액트 리덕스 사용하기 위한 설치**

npm install redux react-redux redux-promise redux-thunk --save

**redux-thunk와 redux-promise의 사용**

redux-thunk는 디스패치한테 객체 아닌 functions으로 받는 법 알려줌

redux-promise는 ``

**리덕스 연결**

index.js에서

import { Provider } from "react-redux";

로 리덕스 연결

index.js에서

그냥 createStore는 promise와 functions를 받을 수 없기 때문에

미들웨어 사용해줌

const createStoreWithMiddleware = applyMiddleware(promiseMiddleware, ReduxThunk)(createStore);

**reducer**

reducer ⇒ 어떻게 state가 변하는지 본 다음 변한값을 리턴

기능마다 reducer을 가지고, redux에서 가져온 combinereducers가 하나로 합쳐준다.

**React Hooks**

- useState, useEffect 등 use가 접두사로 들어가는 함수
- 함수 컴포넌트에서만 사용(클래스 컴포넌트와 달리 함수 컴포넌트가 할 수 없는 부분 보완 위해 사용)
- 컴포넌트 데이터 관리 [ useState, useReducer ]
- 컴포넌트 생명 주기 대응 [ useEffect ]
- 컴포넌트 메서드 호출
- 컴포넌트 간 정보 공유
