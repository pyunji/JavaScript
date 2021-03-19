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
