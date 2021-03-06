# Quest 03. 자바스크립트와 DOM

## Introduction
* 자바스크립트는 현재 웹 생태계의 근간인 프로그래밍 언어입니다. 이번 퀘스트에서는 자바스크립트의 기본적인 문법과, 자바스크립트를 통해 브라우저의 실제 DOM 노드를 조작하는 법에 대하여 알아볼 예정입니다.

## Topics
* 자바스크립트의 역사
* 기본 자바스크립트 문법
* DOM API
  * `document` 객체
  * `document.getElementById()`, `document.querySelector()`, `document.querySelectorAll()` 함수들
  * 기타 DOM 조작을 위한 함수와 속성들
* 변수의 스코프
  * `var`, `let`, `const`

## Resources
* [자바스크립트 첫걸음](https://developer.mozilla.org/ko/docs/Learn/JavaScript/First_steps)
* [자바스크립트 구성요소](https://developer.mozilla.org/ko/docs/Learn/JavaScript/Building_blocks)
* [Just JavaScript](https://justjavascript.com/)

## Checklist
* 자바스크립트는 버전별로 어떻게 변화하고 발전해 왔을까요?
  *

  * 자바스크립트의 버전들을 가리키는 ES5, ES6, ES2016, ES2017 등은 무엇을 이야기할까요?
    * ES = ECMScript : 인터넷 익스플로러와 넷스케이프를 주축으로 호환성을 위해 1997년 부터 시작된 자바스크립트 표준안
    * ES5: use strict, Array Metods, Objext property methods, JSON method 등 도입
    * ES6 = ECMAScript 2015 : let, const, Class, Arrow Fnuctions, Promise 등 도입  
    * ES2016 = ES7 : 제곱 연산자, includes methods 도입
    * ES2017 = ES8 : async/await

  * 자바스크립트의 표준은 어떻게 제정될까요?
    * TC39 위원회에서 회의를 통해서 제정된다. 


* 자바스크립트의 문법은 다른 언어들과 비교해 어떤 특징이 있을까요?
  * 자바스크립트는 객체 기반의 스크립트 언어이고 동적이며 타입을 명시할 필요가 없는 인터프리터(클라이언트의 웹 브라우저에 의해 해석되고 실행) 언어이다. 객체 지향형 프로그래밍과 함수형 프로그래밍을 모두 표현할 수 있다. 
  
  * 자바스크립트에서 반복문을 돌리는 방법은 어떤 것들이 있을까요?
    * for 반복문
    ```
    for (초기화식; 종료 조건; 증감식) {
      // 실행할 코드
    }
    ```
    
    * while 반복문
    ```
    초기화식
    while (종료 조건) {
      // 실행할 코드

      증감식
    }
    ```

    * do ...while 반복문
    ```
    초기화식
    do {
      // 실행할 코드

      증감식
    } while (종료 조건)
    ```
  * DOM: 객체환 된, 또는 객체로 구조화된 문서. 하나의 application는 매우 다양하게 얽힌 객체(object)들로 구성이 되어있으며, 이러한 object들이 구성한 집합을 Document라 한다.
* 자바스크립트를 통해 DOM 객체에 CSS Class를 주거나 없애려면 어떻게 해야 하나요?
  * CSS 선택자 id, class, tag 가 있음
    * DOM 요소를 id 선택자로 접근하는 함수 - getElementById()
    * DOM 요소를 class 값으로 찾아내는 함수 - getElementsByClassName()
    * DOM 요소를 태그 이름으로 찾아내는 함수 - getElementsByTagName()
  * `classList` 속성을 사용하여 추가하거나 제거할 수 있다.
    ```
    const element = document.getElementById("ele")
    
    // class 추가
    function add(event){
      element.classList.add('class1');
    }
    
    // class 제거
    function remove(event){
      element.classList.remove('class1');
    }
    ```
  
  * IE9나 그 이전의 옛날 브라우저들에서는 어떻게 해야 하나요?
    * 호환성 보기를 선택한 경우 작동이 오히려 안되는데 메타태그를 이용해 최신버전 브라우저로 세팅한다.
    ```
    <head>
    <!-- Quirks Mode -->
    <meta http-equiv="X-UA-Compatible" content="IE=5" />

    <!-- IE7 Standards 모드 -->
    <meta http-equiv="X-UA-Compatible" content="IE=7" />

    <!-- IE8 Standards 모드 -->
    <meta http-equiv="X-UA-Compatible" content="IE=8" />

    <!-- 가장 최신 버젼 IE의 Standards 모드 -->
    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

    <!-- DTD가 없는 페이지는 여전히 Quirks Mode로, DTD가 있는 페이지는 IE 7 표준 모드로 렌더링 -->
    <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE7" />
    </haed>
    ```
    
* 자바스크립트의 변수가 유효한 범위는 어떻게 결정되나요?
  * 변수(variable): 데이터를 저장할 때 쓰이는 사용자가 지정한 이름을 사용하는 저장소 
  * 변수의 유효 범위(variable scope): 해당 변수가 접근할 수 있는 변수, 객체 그리고 함수의 집합을 의미한다. 유효 범위에 따라 다음과 같이 구분되다.
    1. 전역변수 (global variable)  
       전역변수는 함수의 외부에서 선언된 변수이다. 코드의 어느 영역에서나 접근할 수 있으며, 웹 페이지가 닫혀야만 메모리에서 사라진다.
       ```
       var vscope = 'global';
       function fscope(){
           console.log(vscope);
       }
       fscope();
       
       // output: global
       ```
       
    2. 지역변수(local variable)
       지역변수는 함수 내에서 선언된 변수이다. 변수가 선언된 함수 내에서만 유효하면, 함수가 종료되면 메모리에서 사라진다. 
       ```
       var vscope = 'global';
       function fscope(){
           var vscope = 'local';
           console.log('함수안 '+vscope);
       }
       fscope();
       console.log('함수밖 '+vscope);
       
       // output: 함수안 local
       // output: 함수밖 global
       ```
       
       * var를 사용하지 않은 지역변수는 전역변수가 된다.
       ```
       var vscope = 'global';
       function fscope(){
           vscope = 'local';
           console.log('함수안'+vscope);
       }
       fscope();
       console.log('함수밖'+vscope);
       
       // output: 함수안 local
       // output: 함수밖 local
       ```

  
  * `var`과 `let`으로 변수를 정의하는 방법들은 어떻게 다르게 동작하나요?
    * var 
      * 변수 중복 선언 가능하여, 예기치 못한 값을 반환할 수 있다.
      * 유효 범위로 인해 함수 외부에서 선언한 변수는 모두 전역 변수가 된다.
      * 변수 선언문 이전에 변수를 참조하면 항상 undefined를 반환한다.
      ```
      var test = "abcd"
      console.log(test);

      var test = "aaabbb"
      console.log(test);
      
      // output: abcd
      // output: aaabbb 
      ```
     
    * let
      * 변수 중복 선언이 불가능하지만, 재할당은 가능하다.
      ```
      let name = '한혜선'
      console.log(name) 
      // output: 한혜선

      let name = '김희재' // output: Uncaught SyntaxError: Identifier 'name' has already been declared

      name = '김희재'
      console.log(name) 
      // output: 김희재
      ```
    
    * const
      * 변수 재선언, 재할당 모두 불가능하다. 반드시 선언과 초기화를 동시에 해야한다.(원시값은 재할당이 불가능하지만 객체는 가능)
      ```
      // 원시값의 재할당
      const name = '한혜선'
      name = '김희재' 
      // output: Uncaught TypeError: Assignment to constant variable.

      // 객체의 재할당
      const name = {
        eng: '한혜선',
      }
      name.eng = '김희재'

      console.log(name) 
      // output: { eng: "김희재" }
      ```

      [더 알아보기](https://gist.github.com/LeoHeo/7c2a2a6dbcf80becaaa1e61e90091e5d)
 
* 자바스크립트의 익명 함수는 무엇인가요?
  * 익명 함수란 변수에 함수의 코드를 저장하는 대신 함수명을 사용하지 않는다. 변수명을 마치 함수명처럼 사용해서 함수를 호출하거나 변수값을 이동시키는데 사용할 수 있다.
  * 단점은 호이스팅이 불가하다. 호이스팅: 함수 선언 보다 함수 호출이 윗 줄에 위치해도 실행되는 기능
   ```
   // 일반 함수 = 함수 선언식
   function 함수명(){
     함수 로직
   }
   
   function SayHello(){
     console.log("hello!");
   }
   SayHello()
   // output: hello!
   
   
   // 익명 함수 
   const sayHello = function() {
     console.log("hello!");
   }
   SayHello()
   // output: hello!
   
   ```

  * 자바스크립트의 Arrow function은 무엇일까요?
    * 기존 함수 표현식에서 function을 삭제하고 인자를 받는 매개변수의 () 와 {} 사이에 화살표를 넣어주면 화살표 함수라 부른다.
      * 화살표 함수는 기본적으로 익명 함수이기 때문에 식으로 변수에 할당해서 사용이 가능하지만, 일반 함수처럼 function 키워드를 이용해 이름을 정의 할 수 없다는 점이 화살표 함수와 함수의 선언 방식에 가장 큰 차이점이다. 화살표 함수와 일반 함수에는 우위가 없으며 상황에 따라 필요한 문법을 이용해 사용하는 것이 좋다. 
    ```
    function example(){
     // 일반함수
    }
    
    
    let arrowFunciotn = () => {
     // 화살표 함수
    }
    ```
     * 함수의 body 표현식이 한 line 이라면 중괄호{} 와 return을 생략할 수 있다.
       ```
       let arrow = () => {
       return "Hello World!"
       }
       arrow()


       let arrow = () => Hello World!
       ```
     * 함수의 매개변수가 하나라면 () 를 생략할 수 있다.
       ```
       let double = (n) => {
        return n * 2
       }
       
       let double = n => n * 2 
       
       // output: double(2) = 4
       ```

## Quest
* (Quest 03-1) 초보 프로그래머의 영원한 친구, 별찍기 프로그램입니다.
  * [이 그림](jsStars.png)과 같이, 입력한 숫자만큼 삼각형 모양으로 콘솔에 별을 그리는 퀘스트 입니다.
    * 줄 수를 입력받고 그 줄 수만큼 별을 그리면 됩니다. 위의 그림은 5를 입력받았을 때의 결과입니다.
  * `if`와 `for`와 `function`을 다양하게 써서 프로그래밍 하면 더 좋은 코드가 나올 수 있을까요?
  * 입력은 `prompt()` 함수를 통해 받을 수 있습니다.
  * 출력은 `console.log()` 함수를 통해 할 수 있습니다.
* (Quest 03-2) skeleton 디렉토리에 주어진 HTML을 조작하는 스크립트를 완성해 보세요.
  * 첫째 줄에 있는 사각형의 박스들을 클릭할 때마다 배경색이 노란색↔흰색으로 토글되어야 합니다.
  * 둘째 줄에 있는 사각형의 박스들을 클릭할 때마다 `enabled`라는 이름의 CSS Class가 클릭된 DOM 노드에 추가되거나 제거되어야 합니다.
* 구현에는 여러 가지 방법이 있으나, 다른 곳은 건드리지 않고 TODO 부분만 고치는 방향으로 하시는 것을 권장해 드립니다.

## Advanced
* Quest 03-1의 코드를 더 구조화하고, 중복을 제거하고, 각각의 코드 블록이 한 가지 일을 전문적으로 잘하게 하려면 어떻게 해야 할까요?
* Quest 03-2의 스켈레톤 코드에서 `let` 대신 `var`로 바뀐다면 어떤 식으로 구현할 수 있을까요?
