# 인터넷 기초[04] 과제2 - 나만의 인공지능 서비스

## 개요
 - 서비스 명 : <span style="background-color:rgb(182,0,80)">오늘의 옷차림</span>
 - 서비스 설명 : 사용자로부터 **나이**, **성별**, **상황**, **날씨**, **기온**을 입력받으면, <span style="background-color:rgb(182,0,80)">오늘의 옷차림</span>는 추천 옷차림을 알려준다. 추가적으로 챙기면 좋은 아이템들도 추천해준다.
 - 서비스 접속 주소 : [https://yummsseo.github.io/styling/](https://yummsseo.github.io/styling/)


## 서비스 구성 요소(1) - Gemini API
- <span style="background-color:rgb(182,0,80)">오늘의 옷차림</span>이 추천하는 옷차림은 구글의 LMM 모델인 Gemini의 API를 활용해 생성한다.
- 활용 모델 : [Gemini-2.0-flash](https://cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/2-0-flash?hl=ko)


## 서비스 구성 요소(2) - 프론트엔드
- <span style="background-color:rgb(182,0,80)">오늘의 옷차림</span> 서비스 페이지는 HTML, CSS, JavaScript를 사용하여 간단하게 구성하였다.
- CSS 스타일 시트는 [style.css](style.css)파일로 따로 분리하였다.


## 서비스 구성 요소(3) - 백엔드
- 구글 Gemini API 호출을 위한 API 키가 노출되지 않도록, 프론트엔드의 요청을 받아서 Gemini API를 호출해주는 간단한 API 백엔드를 구성하였다.
- 해당 백엔드 로직은 서버리스(Severless) 함수 기능을 제공하는 Vercel에 배포했다.
- 코드 및 구현 내용은 [https://github.com/yummsseo/style-api](https://github.com/yummsseo/style-api)를 참고한다.