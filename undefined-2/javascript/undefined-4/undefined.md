# 이벤트 전파\(버블링과 캡처링\)

## 캡처링

위에서 부터 실행.  
잘 사용하지 않음.

## 버블

아래\(안\)에서 부터 실행.  


```javascript
.addEventListener('click', handler, false); 
//세번째는 use capturing 이라고함.
//false는 버블
//event.stopPropagation 멈추는 코드
```

