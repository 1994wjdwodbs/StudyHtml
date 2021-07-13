# JAVASCRIPT

## 자바스크립트 기본 용어와 출력 방법

## 자료형과 변수

## 조건문과 반복문

## 함수

## 객체

## 문서 객체 모델

## 문서 객체 선택 및 조작

## XMLHttpRequest

## AJAX(Asynchronous Javascript And Xml)
웹 브라우저 안에서 처리되는 __자바스크립트(javascript) 기술과 XMLHttpRequest 요청을 접목한 기술__ <br/>
클라이언트 웹브라우저 측에서 웹 서버에 비동기적인 자료 요청, 응답 결과를 화면을 전환하여 새로운 페이지에 출력하지 않도록 처리<br/>

> __AJAX 처리 과정__ <br/>
> XMLHttpRequest 객체 생성<br/>
> 요청에 대한 응답 결과를 처리할 함수 정의( __onreadystate__ )<br/>
> HTML 문서(body)에 응답 결과를 나타낼 요소 표시<br/>

## CORS

Cross-Origin Resource Sharing(CORS)은 추가적인 HTTP header를 사용해서 애플리케이션이 다른 origin의 리소스에 접근할 수 있도록 하는 메커니즘을 말합니다.<br/> 하지만 다른 origin에서 내 리소스에 함부로 접근하지 못하게 하기 위해 사용된다.<br/>

만약 내가 서비스하고 있지 않은 사이트에서 세션을 요청해서 세션을 획득할 수 있다면 해당 사이트는 악의적으로 내 세션을 탈취하거나 다른 행동을 할 수 있습니다.<br/> 그래서 브라우저에서는 이러한 요청을 막습니다. 피싱사이트가 대표적인 공격 사례인데 이러한 것을 막고 내가 허용한 origin들만 요청할 수 있도록 하기 위해 필요합니다.<br/>

브라우저가 리소스를 요청할 때 추가적인 헤더에 정보를 담습니다. 내 origin은 무엇이고 어떤 메소드를 사용해서 요청을 할 것이고 어떤 헤더들을 포함할 것인지를 담아서 서버에 전송합니다.<br/> 서버는 서버가 응답할 수 있는 origin들을 헤더에 담아서 브라우저에게 보냅니다. 브라우저가 이 헤더를 보고 해당 origin에서 요청할 수 있다면 리소스 전송을 허용하고 만약 불가능하다면 에러를 발생시킵니다.<br/>

요청 헤더 목록에는 다음과 같이 있습니다.<br/>

- Origin<br/>
- Access-Control-Request-Method<br/>
preflight요청을 할 때 실제 요청에서 어떤 메서드를 사용할 것인지 서버에게 알리기 위해 사용됩니다.<br/>
- Access-Control-Request-Headers<br/>
preflight요청을 할 때 실제 요청에서 어떤 header를 사용할 것인지 서버에게 알리기 위해 사용됩니다.<br/>

응답 헤더들은 다음과 같이 있습니다.<br/>

- Access-Control-Allow-Origin<br/>
브라우저가 해당 origin이 자원에 접근할 수 있도록 허용합니다. 혹은 '*' 은 credentials이 없는 요청에 한해서 모든 origin에서 접근이 가능하도록 허용합니다.<br/>
- Access-Control-Expose-Headers<br/>
브라우저가 액세스할 수있는 서버 화이트리스트 헤더를 허용합니다.<br/>
- Access-Control-Max-Age<br/>
얼마나 오랫동안 preflight요청이 캐싱 될 수 있는지를 나타낸다.<br/>
- Access-Control-Allow-Credentials <br/>
LCredentials가 true 일 때 요청에 대한 응답이 노출될 수 있는지를 나타냅니다.<br/>
preflight요청에 대한 응답의 일부로 사용되는 경우 실제 자격 증명을 사용하여 실제 요청을 수행 할 수 있는지를 나타냅니다.<br/>
간단한 GET 요청은 preflight되지 않으므로 자격 증명이 있는 리소스를 요청하면 헤더가 리소스와 함께 반환되지 않으면 브라우저에서 응답을 무시하고 웹 콘텐츠로 반환하지 않습니다.<br/>
- Access-Control-Allow-Methods<br/>
preflight요청에 대한 대한 응답으로 허용되는 메서드들을 나타냅니다.<br/>
- Access-Control-Allow-Headers<br/>
preflight요청에 대한 대한 응답으로 실제 요청 시 사용할 수 있는 HTTP 헤더를 나타냅니다.<br/>



## jQuery 라이브러리



[이전](https://github.com/1994wjdwodbs/StudyHtml)
