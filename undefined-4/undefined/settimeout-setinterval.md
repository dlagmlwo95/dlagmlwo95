# setTimeout / setInterval

### setTimeout : 일정시간이 지난후 함수를 실행

```javascript
const tId = function showName(name){
    console.log(name);
}
setTimeout(showName,3000,'m');
clearTimeout(tid);
```

### setInterval : 일정시간 간격으로 함수를 반복 

```javascript

let num = 0;
function showName(){
    console.log(`접속하신지 ${num++}초가 지났습니다);
    if(num > 5){
        clearInterval(tId);
}
const tId = setInterval(showTime,1000);

```

