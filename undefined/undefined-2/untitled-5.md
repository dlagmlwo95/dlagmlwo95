# 11. 비동기, Call back

자바스크립트의 비동기 처리  
callback  
promise   
async / await

hosting : 변수와 함수선언들이 자동적으로 제일 위로 올라가는 것.



## 동기 Synchronous Callback

정해진 순서에 맞게 

## 비동기 Asynchronous callback

언제실행될지 모름

```javascript
console.log('1');
setTimeout(() => console.log('2'),1000);
console.log('3');
//1,3,2
```

