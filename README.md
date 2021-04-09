# JavaScript Essential Training

#### Author: Tackhyun Jung

#### Status: ~ing

## References

* 자바스크립트 공식 사이트 : ecma-international.org
* 자바스크립트 문법 참조 사이트 : develpoer.mozilla.org

## Script async와 defer의 차이

일반적으로 js를 참조하게 되면 한줄씩 parsing하여 DOM 요소로 변환함
<script> 태그를 발견하면, 서버에서 해당 파일을 다운로드 받게 됨(latency가 발생)

* 기본 참조방식 
```javascript
<head> or <body>
  <script src="test.js"></script>
</head> or </body>
```
-> 이러한 방식으로 참조하게 되면 js를 fetching 하는것을 기다려야 함

* head + async 참조방식
```javascript
<head>
  <script asyn src="test.js"></script>
</head>
```
-> 브라우저가 parsing의 과정에서 asyn을 병렬로 수행하게 하고 pasing을 지속함. 
-> parsing 종료된 이후 다시 js를 참조하는 방식
-> 장점: 다운로드 받는 시간 절약
-> 단점: html이 js가 다운로드 되기 전에 실행되기 때문에 기능이 동작하지 않을 수 있음



```
