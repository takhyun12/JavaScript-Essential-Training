## Script async와 defer의 차이

일반적으로 js를 참조하게 되면 한줄씩 parsing하여 DOM 요소로 변환함.

스트립트 태그를 발견하면, 서버에서 해당 파일을 다운로드 받게 됨(latency가 발생).

### 기본 참조방식

```javascript
<head> or <body>
    <script src="test.js"></script>
</head> or </body>
```

* 이러한 방식으로 참조하게 되면 js를 fetching 하는것을 기다려야 함. (비효율적)

### head + async 참조방식

```javascript
<head>
    <script asyn src="test.js"></script>
</head>
```

* 브라우저가 parsing의 과정에서 js 다운로드를 병렬로 수행하게 하고 parsing을 지속함. 
* 병렬로 수행된 js 다운로드가 완료되면 parsing을 다시 멈추고 참조하는 방식
* 여러개의 js 파일을 다운로드 하는 경우에는 먼저 다운로드가 끝난 순서대로 참조됨
* 장점: 다운로드 받는 시간 절약
* 단점: html이 js가 다운로드 되기 전에 실행되기 때문에 기능이 동작하지 않을 수 있음

### head + defer 참조방식

```javascript
<head>
    <script defer src="test.js"></script>
</head>
```

* 브라우저가 parsing의 과정에서 js 다운로드를 병렬로 수행하게 하고 parshing을 지속함.
* parsing이 끝난 이후, 다운로드된 js 파일을 실행함
* 여러개의 js 파일을 다운로드 하는 경우에는 개발자가 정의한 순서대로 참조
