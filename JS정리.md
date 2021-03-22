# 일단 막 쓰고 나중에 정리해 일단 뭐든 쓰는게 중요
```
Run JavaScript
- Event handler
- <script>
- console

DataType
- String
- Number
- Variable
- Boolean
- Array
- Object

Operator
- Arithmetic operation
- Assignment operators
- Comparison operator

Statement
- Conditional statement
- Loop statement
- Loop & Array 배열
- Loop & Object
- Property & Method

Refactoring

Web browser
- Select element
- Attribute

CSS
- Style attribute
- Style tag
- selector

```

## 수업의 목적
- JS는 사용자와 상호작용하는 언어다
- 웹 브라우저는 한 번 화면에 출력되면 자기 자신을 바꿀 수 없다.
    - 하지만 JS를 이용해 HTML을 제어할 수 있다.
- JS는 웹페이지를 동적으로 만들어준다.

## HTML과 JavaScript의 만남 1 (script 태그)
- JS는 HTML 위에서 동작하는 언어이다.
- HTML은 `<script></script>` 태그 안쪽의 코드를 JS로 해석한다
- HTML에서의 1+1은 그대로 1+1이지만, JS에서의 1+1은 2로 출력된다.

```HTML
<body>
    <h1>JavaScript</h1>
    <script>
    document.write(1+1);
    </script>
    <h1>html</h1>
    1+1
</body>
```

## HTML과 JavaScript의 만남 2 (이벤트)
- 이벤트: 웹브라우저 위에서 일어나는 일
    - on어쩌고 속성을 event라고 한다.
- 이벤트는 JS와 사용자가 상호작용하는데 핵심적인 역할을 한다.
- `onclick`속성
    - 해당 속성의 value는 반드시 JS가 와야한다.
    - 어떤 이벤트가 일어났을 때 JS가 실행되게하는 것이 onclick이다.

```html
<body>
    <input type="button" value="hi" onclick="alert('hi')">
    <input type="text" onchange="alert('changed')">
    <input type="text" onkeydown="alert('key down!')">
</body>
```
## HTML과 JavaScript의 만남 3 (콘솔)
- 관리자도구에서 console 이용하면 파일을 만들지 않고도 현재 켜져있는 웹페이지에서 JS코드를 즉석으로 실행할 수 있다.

## 데이터타입 - 문자열과 숫자

## 변수와 대입 연산자
- variable vs constant
- `var 변수명 = 값;`

## 제어할 태그 선택하기
- 버튼을 클릭 시 body태그의 css 속성을 바꿔야 한다.
- `document.querySelector("선택자").style.속성설정;`

## 프로그램, 프로그래밍, 프로그래머
- HTML은 컴퓨터 언어이지만 컴퓨터 프로그래밍 언어는 아니다.
- JS는 컴퓨터 언어이면서 컴퓨터 프로그래밍 언어이다.
## 문법
### if...else if...else문
```js
if (condition) {
  code to run if condition is true
} else {
  run some other code instead
}
```
### 비교연산자
|비교연산자|의미|
|---|---|
|`===`, `!==`|한 값이 다른 값과 같거나 다른지 테스트 한다.|
|`<`, `>`|한 값이 다른 값보다 작은지 큰지 테스트 한다.|
|`<=`, `>=`|한 값이 다른 값보다 작거나 같은지, 크거나 같은지 테스트 한다|

### 논리연산자
|논리연산자|의미|
|---|---|
|`&&`|AND|
|`||`|OR|
|`!`|NOT|

### switch 문
```js
switch (expression) {
  case choice1:
    run this code
    break;

  case choice2:
    run this code instead
    break;

  // include as many cases as you like

  default:
    actually, just run this code
}
```
## 리팩토링
```js
<input id="night_day" type="button" value="night" onclick="
    if(document.querySelector('#night_day').value === 'night'){
        document.querySelector('body').style.backgroundColor = 'black';
        document.querySelector('body').style.color = 'white';
        document.querySelector('#night_day').value = 'day';
    } else {
        document.querySelector('body').style.backgroundColor = 'white';
        document.querySelector('body').style.color = 'black';
        document.querySelector('#night_day').value = 'night';
    }

">
```
- this의 사용으로 중복 제거
```js
<input type="button" value="night" onclick="
    if(this.value === 'night'){
        document.querySelector('body').style.backgroundColor = 'black';
        document.querySelector('body').style.color = 'white';
        this.value = 'day';
    } else {
        document.querySelector('body').style.backgroundColor = 'white';
        document.querySelector('body').style.color = 'black';
        this.value = 'night';
    }

">
```
- 또 중복되는 것을 지구끝까지 쫓아가서 제거 ㅋㅋㅋㅋ
    - 변수의 사용
```html
<input type="button" value="night" onclick="
    var target = document.querySelector('body');
    if(this.value === 'night'){
        target.style.backgroundColor = 'black';
        target.style.color = 'white';
        this.value = 'day';
    } else {
        target.style.backgroundColor = 'white';
        target.style.color = 'black';
        this.value = 'night';
    }

">
```
## 함수
### 함수의 기본 문법
```js
function myFunction(){
    do something
}
```
### Parameter & Argument
- 매개변수(parameter): 사용자에게 전달받은 값을 저장하며 함수 내에서 사용되는 변수 이름
- 인자(argument): 매개변수에 전달된 값 자체

### return

### this, self
- 독립된 함수로 만들었다면 this(지역)와 self(전역)를 잘 사용해야함
- 메소드나 프로퍼티가 속해있는 객체를 지칭할 때 this로 표현함.
## 객체
```js
var objectName = {
  member1Name: member1Value,
  member2Name: member2Value,
  member3Name: member3Value
};
```
### 프로퍼티와 메소드

## jquery라이브러리
- cdn 가져오기: 
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
``ㅁ`
 ```js
var alist = document.querySelectorAll('a');
        var i = 0;
        while (i < alist.length) {
            alist[i].style.color = color;
            i += 1;
        }
```
```js
$('a').css('color', color);
```