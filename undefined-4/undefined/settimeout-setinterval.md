# setTimeout / setInterval

### setTimeout : 일정시간이 지난후 함수를 실행

```javascript
려ㅜfunction showName(name
let num = 0;
function showName(){
    console.log(`접속하신지 ${num++}초 지났습니다);
}
const tId = setTimeout(showName,3000,'Mike')
clearInterval(tId);
```

### setInterval : 일정시간 간격으로 함수를 

