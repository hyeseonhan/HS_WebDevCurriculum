# Quest 01. HTML과 웹의 기초

## Introduction
* HTML은 HyperText Markup Language의 약자로, 웹 브라우저에 내용을 표시하기 위한 가장 기본적인 언어입니다. 이번 퀘스트를 통해 HTML에 관한 기초적인 사항들을 알아볼 예정입니다.

## Topics
* HTML의 역사
  * HTML 4.01, XHTML 1.0, XHTML 1.1
  * XHTML 2.0과 HTML5의 대립
  * HTML5와 현재
* 브라우저의 역사
  * Mosaic와 Netscape
  * Internet Explorer의 독점시대
  * Firefox와 Chrome의 등장
  * iOS Safari와 모바일 환경의 브라우저
  * Edge와 Whale 등의 최근의 Chromium 계열 브라우저
* HTML 문서의 구조
  * `<html>`, `<head>`와 `<body>` 등의 HTML 문서의 기본 구조
  * 시맨틱 엘리먼트
  * 블록 엘리먼트와 인라인 엘리먼트의 차이

## Resources
* [MDN - HTML](https://developer.mozilla.org/ko/docs/Web/HTML)
* [HTML For Beginners](https://html.com/)
* [History of the web browser](https://en.wikipedia.org/wiki/History_of_the_web_browser)
* [History of HTML](https://en.wikipedia.org/wiki/HTML)
* [StatCounter](https://gs.statcounter.com/)

## Checklist
1. HTML 표준의 역사는 어떻게 될까요?
 </br>‣ 1991년-HTML1.0 -> 1994년-W3C -> 1995년-HTML2.0 -> 1997년-HTML3.2 -> 1999년-HTML4.01 -> 2000년-XHTML1.0
 
   </br> 1.1 HTML 표준을 지키는 것은 왜 중요할까요?
    </br>‣ 표준이 없었던 때에 개발자들은 익스플로러와 넷스케이프 두 개의 브라우저에 맞춰 두 가지 사이트를 개발해야했습니다. 다른 경우로 최신 브라우저들이 만들어지면서 익스플로러 전용 코드가 이 브라우저들과 호환되지 않는 문제가 발생하였습니다. 이는 많은 노동력과 시간을 낭비하고 비용 또한 증가합니다. 따라서 표준을 지키면 효율적으로 웹을 만들고, 모든 브라우저에서 이용이 가능합니다. 

   </br> 1.2 XHTML 2.0은 왜 세상에 나오지 못하게 되었을까요?
   </br>‣ XML1.0으로 HTML 4.01을 새로 만든 버전인데, 엄격한 태그 작성으로 개발자들에게 어려움을 주고, 문법이 잘못될 경우 페이지가 표시되지 않는 문제로 사용자들이 사라졌다. 
    
   </br> 1.3 HTML5 표준은 어떤 과정을 통해 정해질까요?
    </br>‣
    
    
2. 브라우저의 역사는 어떻게 될까요?
 </br>‣ 최초의 웹 브라우저는 팀 버너스 리가 WorldWideWeb 이라는 이름으로 1990년에 발명하였다. 후에 Nexus로 이름이 바뀌었다. 1993년에 Marc Andreessen이 이미지 표현이 가능한 최초의 그래픽 웹 브라우저 Mosaic를 만들었다. 1994년에 Marc Andreessen이 Netscape를 설립하고 후에 Netscape Navigator 브라우저를 개발하면서 Mosaic는 중단되었다. Microsoft가 Mosaic 소스코드를 이용해서 Internet Explorer를 개발하였다.

   </br> 2.1 Internet Explorer가 브라우저 시장을 독점하면서 어떤 문제가 일어났고, 이 문제는 어떻게 해결되었을까요?
   </br>‣ 2001년 8월 버전 6을 출시 후로 개발을 거의 중단하다시피 하였고, 5년간 2번의 서비스 팩 업데이트 이외에는 기능 개선이 거의 이루어지지 않았습니다. 그리고 PC 중심이 였던 익스플로러는 스마트폰에 지원하지 않아 웹사이트가 구동되지 않은 상황이 발생하였다. 또 보안에 취약하고 웹 표준 언어 HTML5와 호환성이 떨어지는 문제가 발생하였다. 새로운 브라우저들의 등장으로 익스플로러의 독점은 해소되어가고 있다.

   </br> 2.2 현재 시점에 브라우저별 점유율은 어떻게 될까요? 이 브라우저별 점유율을 알아보는 것은 왜 중요할까요?
   </br>‣ 개발자는 브라우저나 버전간의 호환성을 생각하면서 코드를 작성해야하기 때문에 브라우저별 점유율을 파악하는게 중요하다고 생각된다.
   </br><img width="925" alt="스크린샷 2021-12-03 오전 4 12 36" src="https://user-images.githubusercontent.com/68494080/144487580-1b79fd18-ebf3-4b86-97cb-cc64e1c80ae6.png"> 

   </br> 2.3 브라우저 엔진(렌더링 엔진)이란 무엇일까요? 어떤 브라우저들이 어떤 엔진을 쓸까요?
   </br>‣ 브라우저 엔진은 모든 웹 브라우저의 핵심 소프트웨어 구성요소이다. 브라우저 엔진의 주된 역할은 사용자에게 HTML 문서와 웹 페이지의 resources를 상호작용적인 시각표현으로 변환시켜 준다.(내용 정보 인 HTML,XML과 서식 정보 CSS 등을 사람이 읽을 수 있는 문서로 표시)
   * Gecko engine: FireFox, Thunderbird email client, SeaMonkey internet suite
   * Webkit engine : Safari, Chrome -> Webkit2 engine: Safari, Blink engine: Chrome
   
   </br> 2.4 모바일 시대 이후, 최근에 출시된 브라우저들은 어떤 특징을 가지고 있을까요?
   </br>‣


3.HTML 문서는 어떤 구조로 이루어져 있나요?
</br>‣

</br> 3.1 `<head>`에 자주 들어가는 엘리먼트들은 어떤 것이 있고, 어떤 역할을 할까요?
</br>‣

</br> 3.2 시맨틱 태그는 무엇일까요?
</br>‣

</br>3.2.1 시맨틱 엘리먼트를 사용하면 어떤 점이 좋을까요?
</br>‣ 
</br>3.2.2 `<section>`과 `<div>`, `<header>`, `<footer>`, `<article>` 엘리먼트의 차이점은 무엇인가요?
</br>‣

 </br> 3.3 블록 레벨 엘리먼트와 인라인 엘리먼트는 어떤 차이가 있을까요?
 </br>‣

## Quest
* [이 화면](screen.png)의 정보를 HTML 문서로 표현해 보세요. 다만 CSS를 전혀 사용하지 않고, 문서의 구조가 어떻게 되어 있는지를 파악하여 구현해 보세요.
  * [CSS Naked Day](https://css-naked-day.github.io/)는 매년 4월 9일에 CSS 없는 웹 페이지를 공개하여 내용과 마크업에 집중한 HTML 구조의 중요성을 강조하는 행사입니다.
* 폴더에 있는 `skeleton.html` 파일을 바탕으로 작업해 보시면 됩니다.
  * 화면을 구성하는 큰 요소들을 어떻게 처리하면 좋을까요?
  * HTML 문서상에서 같은 층위에 비슷한 요소들이 반복될 때는 어떤 식으로 처리하는 것이 좋을까요?

## Advanced
* XML은 어떤 표준일까요? 어떤 식으로 발전해 왔을까요?
* YML, Markdown 등 다른 마크업 언어들은 어떤 특징을 가지고 있고, 어떤 용도로 쓰일까요?
