# JavaScript Essential Training

#### Author: Tackhyun Jung

#### Status: ~ing

## References

* 자바스크립트 공식 사이트 : ecma-international.org
* 자바스크립트 문법 참조 사이트 : develpoer.mozilla.org

## Script async와 defer의 차이
```
일반적으로 head안에 js를 참조하게 되면 한줄씩 parsing하여 DOM 요소로 변환함
<script> 태그를 발견하면, 서버에서 해당 파일을 다운로드 받게 됨(latency가 발생 할 수 있음)

* 일반적인 참조방식 
<head> or <body>
  <script src="test.js"></script>
</head> or </body>

-> 이러한 방식으로 참조하게 되면 js를 fetching 하는것을 기다려야 함




```
