# call, apply, bind

함수호출 방식과 관계없이 this를 지정 할 수 있음

## call

콜 메소드는 모든 함수에서 사용할 수 있으며 this를 특정값으로 지정할 ㅜ 있습니다.

```javascript
//call
const mike ={
    name:'mike',
};
const tom = {
    name:'tom'
};

function showThisName(){
    console.log(this.name);
}
showThisName();
showThisName.call(mike);
//call의 첫번째 매개변수는 this로 사용할 값이고 매개변수가 더
//으면 그 매개변수로 호출하는 함수로 전달됨.

function update(birth,job){
    this.birth = birth;
    this.job = job;
};
update.call(mike, 1999, 'singer');
console.log(mike);

update.apply(mike, [1999, 'singer']);
console.log(mike);

update.call(tom, 1988, 'teacher');
console.log(tom);
update.apply(tom, [1988, 'teacher']);
console.log(tom);
```

## apply 

배열 요소를 함수 매개변수로 사용할 때   
두번째 매개변수로 배열을 전달하면 그 요소들을 차례대로 인수로 





```javascript
const nums = [3,10,1,6,4];
//const minNum = Math.min(...nums);
//const maxNum = Math.max(...nums);
const minNum = Math.min.apply(null, nums);
const maxNum = Math.max.call(null, ...nums); //call은 ...nums

console.log(minNum);
console.log(maxNum);
```

