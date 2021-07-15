# 구조 분해 할당

구조 분해 할당\(destructuring assignment\)  
구조 분해 할당 구문은 배열이나 객체의 속성을 분해해서 그 값을 변수에 담을 수 있게 하는 

```javascript
let [x, y] = [1, 2];
console.log(x) // 1
console.log(y) // 2

let users = ['m','t','j'];
let [user1,user2,user3] = users;
//해석 : let user1 = users[0]
//해석 : let user2 = users[1]
//해석 : let user3 = users[2]

//기본값
let [a,b,c] = [1,2]; //c undefined
let [ a=3,b=4,c=5] = [1,2];
console.log(a); //1
console.log(b); //2
console.log(c); //5


//일부 반환값 무시
let [user1, ,user2] = ['m','t','j','t'];
console.log(user1); //m
console.log(user2); //j
```



