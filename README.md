# front-dev-basics 
프론트엔드 기초를 학습하는 레포지토리입니다. 
___

## Javascript
- Javascript는 Single Thread
- 특정 코드의 연산이 끝날 때까지 코드의 실행을 멈추지 않고, 다음코드를 먼저 실행하는게 Javascript의 비동기 처리
- Event loop는 call stack을 지켜보다 비어있으면 Queue에 적재된 task를 실행
- Promise의 callback함수는 Microtask Queue에 적재
- <details>
    <summary>Javascript 비동기 심화 탐구 </summary> 
  
  - 하나의 Call Stack만을 가지고 있고, 한 번에 하나의 Task만 처리 
  
  - Promise, async/await와 같은 비동기 호출의 Callback 함수들은 Microtask Queue에 담기게 되고 FIFO(First In First Out)의 형태로 실행
  
  - Eventloop는 현재 실행중인 Task가 있는지, Queue들에 적재된 Task가 있는지 주기적으로 확인
  
  </details>
___

## Jquery 
>  jQuery는 HTML의 DOM 조작과 이벤트 제어, 애니메이션 그리고 Ajax까지 웹 화면을 다루는 자바스크립트 라이브러리

- jQuery는 클라이언트 측 HTML 스크립팅을 간소화하기 위해 고안된 크로스 플랫폼 자바스크립트 라이브러리
- jQuery의 위력은 DOM을 쿼리 (그래서 이름이 jQuery) & 잘 문서화된 API를 사용해 조작 가능 

<jquery 기능>
- DOM과 관련된 처리를 쉽게 구현 가능
- 규칙성을 가지고 이벤트를 처리 가능 
- 애니메이션 효과 쉽게 만들기 가능 
- AJAX 처리 방식 편리하게 사용 가능
___
### Javascript vs Jquery 

> jQuery는 작은 양의 코드로 Javascript로 작성된 많은 양의 코드와 동일한 동작 가능
 
- javascript
```js
var titleElements = document.getElementsByClassName("title"); 

for (var titleElement in titleElements) {
   titleElement.className = titleElement.className + " selected"; 
}
```

- jquery 
```js
$(".title").addClass("selected");
```
=> jQuery를 사용하여 HTML 요소를 선택하고 해당 요소에 CSS 클래스를 추가하는 코드 
___

## Ajax 
. Ajax는 웹 페이지가 전체 페이지를 새로고침하지 않고도 서버를 호출하고, 응답을 처리하고, 페이지의 일부를 업데이트할 수 있는 근본적인 방법

> 서버와 클라이언트(사용자)간에 데이터를 이동하고 화면을 구성하는 구현 방식

- 데이터를 이동하고 화면을 구성하는데 있어서 웹 화면을 갱신하지 않고 필요한 데이터를 서버로 보내고 가져오는 방법
- 화면 갱신이 없어서 사용자 입장에서는 매우 편리하고 빠르게 작업을 처리하는 것처럼 느끼기 가능
- 그러나, 동적으로 화면을 구성하는 만큼 개발자 구현 복잡 

![image](https://www.nextree.co.kr/content/images/2021/01/jsseo-140509-ajax-05-1024x527.png)
- Ajax 통신에 대한 그림
- 비동기 식으로 데이터 전송 진행
- 위 그림2 처럼 서버로 데이터를 요청하고 응답을 기다리는 동안 웹은 자신의 다른 업무 진행
- 응답이 오면 그 후 작업 진행
-> 사용자 입장에서는 화면 갱신도 없고, 요청-응답 사이 시간에도 다른 일을 진행 할 수 있기 때문에 편리하고 빠르게 작업을 처리하는 것처럼 느껴짐 

### Reference

[Javascript 비동기 함수의 동작원리 (feat. EventLoop)]([https://www.nextree.co.kr/p9521/](https://gruuuuu.github.io/javascript/async-js/))

[JavaScript, jQuery, 그리고 Ajax POST](https://www.Tnextree.co.kr/p9521/)

[jQuery란 무엇인가?]([https://www.Tnextree.co.kr/p9521/](https://code.tutsplus.com/ko/what-is-jquery--cms-26232t)https://code.tutsplus.com/ko/what-is-jquery--cms-26232t)

