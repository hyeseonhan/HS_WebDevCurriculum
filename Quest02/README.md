# Quest 02. CSS의 기초와 응용

## Introduction
* CSS는 Cascading StyleSheet의 약자입니다. 웹브라우저에 표시되는 HTML 문서의 스타일을 지정하는 (거의) 유일하지만 다루기 쉽지 않은 언어입니다. 이번 퀘스트를 통해 CSS의 기초적인 레이아웃 작성법을 알아볼 예정입니다.

## Topics
* CSS의 기초 문법과 적용 방법
  * Inline, `<style>`, `<link rel="stylesheet" href="...">`
* CSS 규칙의 우선순위
* 박스 모델과 레이아웃 요소
  * 박스 모델: `width`, `height`, `margin`, `padding`, `border`, `box-sizing`
  * `position`, `left`, `top`, `display`
  * CSS Flexbox와 Grid
* CSS 표준의 역사
* 브라우저별 Developer tools

## Resources
* [MDN - CSS](https://developer.mozilla.org/ko/docs/Web/CSS)
* [Centering in CSS: A Complete Guide](https://css-tricks.com/centering-css-complete-guide/)
* [A complete guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [그리드 레이아웃과 다른 레이아웃 방법과의 관계](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Grid_Layout/%EA%B7%B8%EB%A6%AC%EB%93%9C_%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83%EA%B3%BC_%EB%8B%A4%EB%A5%B8_%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83_%EB%B0%A9%EB%B2%95%EA%B3%BC%EC%9D%98_%EA%B4%80%EA%B3%84)

## Checklist
* CSS를 HTML에 적용하는 세 가지 방법은 무엇일까요?
</br>‣ 1. External CSS: 외부에서 스타일 시트 파일을 불러오는 방식
  ```
  <head>
   <link rel="stylesheet" type="text/css" href="example.css">
  </head>
  ```
  
  </br>‣ 2. Internal CSS: HTML 파일 내부에서 style을 정하는 방식
     ```
       <head>
           <style>
               body { background-color: lightyellow; }
               h2 { color: red; text-decoration: underline; }
           </style>
       </head>
     ```
    
  </br>‣ 3. Inline CSS: HTML 요소 내부에 style 속성을 사용해서 적용하는 방식
     ```
      <p style="color:gray;"></p>
     ```
   
   </br>

  * 세 가지 방법 각각의 장단점은 무엇일까요?
  </br>‣ 1. External CSS: 장점은 전체적인 스타일을 일관성 있게 유지할 수 있고, 일괄적으로 변경할 수 있어 효율성이 높다. 단점은 외부에서 스타일 시트를 관리해야하므로 번거러움이 있다.
  </br>‣ 2. Internal CSS: 장점은 HTML 문서 안에서 여러가지 요소를 한번에 꾸밀 수 있고, 단점은 다른 문서에 적용할 수 없다.
  </br>‣ 3. Inline CSS: 장점은 직관적으로 사용할 수 있고 단점은 내용과 스타일이 분리되지 않아 스타일 일괄 변경시 효율성이 떨어진다.

* CSS 규칙의 우선순위는 어떻게 결정될까요?
   1. 속성값 뒤의 !important : 우선선위를 무시하고 !important 붙이면 상위 우선 순위가 되다.
   2. 태그에 linline으로 스타일 속성 지정
   3. 선택자가 #id 
   4. 선택자가 .class 및 pseudo(추상) 클래스(ex. :hover)
   5. 선택자가 tag 이름
   6. 상위 객체에 의해 상속된 속성


* CSS의 박스모델은 무엇일까요? 박스가 화면에서 차지하는 크기는 어떻게 결정될까요?
</br>‣ 박스모델: 모든 HTML 요소는 박스 모양으로 구성되며, 이것을 박스 모델이라 부른다.
</br>‣ 박스모델은 HTML 요소를 padding, border, margin, content로 구분한다.
  </br>![img_css_boxmodel](https://user-images.githubusercontent.com/68494080/144715820-80d5aedc-c8c6-47fb-b292-307a09b2879b.png)


* `float` 속성은 왜 좋지 않을까요?
</br>‣ float: 한 요소가 주변의 다른 요소와 어떻게 함께 배치할 것인가 결정하는 속성.
텍스트와 이미지를 정렬할 때 쓰면 편리한 속성이다. overflow 속성이 visible인 상태에서는 부모 요소의 크기가 자동으로 늘어나지 않는다. 요소들의 높이가 제각각이라면 정렬이 깨질 수 있다. float는 요소의 흐름을 관리하는 속성이기 때문에 속성이 다음 요소로 상속된다. 이런 문제 때문에 좋지 않다.


* Flexbox(Flexible box)와 CSS Grid의 차이와 장단점은 무엇일까요?
  * Flexbox: 1차원으로 수평, 수직 영역 중 하나의 방향으로만 레이아웃을 나눌 수 있다.
    * 모든 방향으로 정렬이 가능하고, reverse도 가능하다. Container로 사용할 경우, 하위 item들을 정렬하기가 매우 수월하다. 단점은 레이아웃을 정의하기에는 직관적이 않다.  
  * Grid: 2차원으로 수평 수직을 동시에 영역을 나눌 수 있다.
    *  prototyping할 때 매우 쉽고 효율적으로 간단하게 작성하여 2차원의 레이아웃을 관리할 수 있다. 유일한 단점은 브라우저 호환성이다.   
  ![1_fIZIpw-jvsUa3yNIpl8zHw](https://user-images.githubusercontent.com/68494080/144716736-f6da4a83-ffed-466e-a65d-df2168b790cc.png)


* CSS의 비슷한 요소들을 어떤 식으로 정리할 수 있을까요?

## Quest
* Quest 01에서 만들었던 HTML을 바탕으로, [이 그림](screen.png)의 레이아웃과 CSS를 최대한 비슷하게 흉내내 보세요. 꼭 완벽히 정확할 필요는 없으나 align 등의 속성은 일치해야 합니다.
* **주의사항: 되도록이면 원래 페이지의 CSS를 참고하지 말고 아무것도 없는 백지에서 시작해 보도록 노력해 보세요!**

## Advanced
* 왜 CSS는 어려울까요?
* CSS의 어려움을 극복하기 위해 어떤 방법들이 제시되고 나왔을까요?
* CSS가 브라우저에 의해 해석되고 적용되기까지 내부적으로 어떤 과정을 거칠까요?
* 웹 폰트의 경우에는 브라우저 엔진 별로 어떤 과정을 통해 렌더링 될까요?
