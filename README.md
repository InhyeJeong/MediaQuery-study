# MediaQuery-study
* 반응형 웹페이지를 위한 미디어쿼리 스터디 레파지토리입니다.
* @media 브라우저 지원

```
ie9+, chrome 21+, firefox3.5+, safari4.0+, opera 9+
```

## 1. 미디어 쿼리 사용법
* css 내부 삽입

```html
<!-- link요소에 있어서의 CSS 미디어 쿼리 -->
<link rel="stylesheet" media="(max-width: 800px)" href="example.css" />
```

* 링크 연결
```html
<!-- 스타일 이벤트 내의 CSS 미디어 쿼리 -->
<style>
@media (max-width: 600px) {
  .container {
    display: none;
  }
}
</style>
```

## 2. 미디어 쿼리 문법
### 1) 연산자
```
and | not | only | ,
```
* **and 연산자** : 여러 미디어 특징들을 하나로 결합
* **, (or) 연산자** :  쉼표로 분리된 각 목록은 각각 개별 미디어 퀴리임
* **not 연산자** : 전체 미디어 쿼리를 부정하기 위해 사용
* **only 연산자** : 미디어 쿼리를 지원하지 않는 브라우저가 주어진 스타일을 적용하는 것을 방지
( not이나 only를 사용하려면 미디어 타입을 규정해야함 / 미디어 쿼리는 대소문자 구별x)

```html
@media (min-width: 700px) {background-color: yellow;}
```
* 위 구문에서 미디어 타입 생략되어 있지만, 미디어 타입의 기본값은 **all = @media all and(min-width: 700px) {...}**
#### ① and 연산자의 사용

* 새로운 미디어 특징들을 추가할 때마다 and 연산자 사용 : 모든 유형의 장치이며 최소너비 700px, 세로방향 모드일 때만 적용한다는 뜻

```html
@media (min-width: 700px) and (orientation:portrait) {...}
```
