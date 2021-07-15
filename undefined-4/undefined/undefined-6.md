# 나머지 매개변수, 전개구문

### 인수 전달

```javascript
function showName(name){
    console.log(name);
}
showName('Mike'); //mike
showName('Mike','Tom'); // mike
showName(); //undefined
```

### arguments : 화살표함수에는 X 

함수로 넘어 온 모든 인수에 접근  
함수 내에서 이용 가능한 지역 변수  
length/index  
Array 형태의 객체  
배열의 내장 메서드없음\(forEach,map\)

