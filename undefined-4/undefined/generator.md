# Generator

## Generator

**함수의 실행을 중간에 멈췄다가 재개할 수 있는 기능  
다른작업을 하다가 다시 돌아와서 next\(\)를 해주면 멈췄던 부분부터 이어서   
값**을 미리 만들어 두지 않음\(그때그때생성\)

```javascript
//generator은 function옆에 *을 써서 만든다
//내부에서 yield키워드를 사용한다.
function* fn(){
  console.log(1);
  yield 1;
  console.log(2);
  yield 2;
  console.log(3);
  console.log(4);
  yield 3;
  return 'finish';
}
const a = fn();
```



### iterable\(반복이 가능하다 의미\)

* Symbol.iterator 메서드가 있다.
* Symbol.iterator 는 iterator를 반환해야한다.addClass

### iterator

* next메서드를 가진다
* next메서드는 value와 done 속성을 가진 객체를 반환한다.
* 작업이 끝나면 done은 true가 된다.



```javascript

function* fn(){
  yield 4;
  yield 5;
  yield 6;
}
const a = fn();
a[Symbol.iterator]() === a; //true

for (let num of a ) {
  console.log(num);
}// 456
//문자열도가능
```

