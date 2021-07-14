# 객체 메소드

## computed property

```javascript
let a = 'age';
const user = {
    name : 'Mike',
    [a] : 30 // 대괄호를 사용해서 사용 가능 ㅣ것을 computed property라고 
}
```

## 자주쓰는 메소드

### Object.assign \(\) :객체복제

키가 같다면 덮어쓰게 된다.

### Object.keys\(\) :  키 배열로 반환

```javascript
const user = {
    name : 'mike',
    age : 30,
    gender : 'male',
}
Object.keys(user); //["name","age","gender"]
```

### Object.values\(\) :  값 배열로 반환

```javascript
const user = {
    name : 'mike',
    age : 30,
    gender : 'male',
}
Object.values(user); //["mike",30,"male"]
```

### Object.entries\(\):키/값 배열반

```javascript
const user = {
    name : 'mike',
    age : 30,
    gender : 'male',
}
Object.entries(user); //["name","mike" "age",30 "gender","male"]
```

### Object.fromEntries\(\) : 키/값 배열을 객체로  

```javascript
const arr = [
   ['name':'mike'],
   ['age':30],
   ['gender': 'male']
]
Object.fromEntries(arr);

/*{
    name:'mike',
    age:30,
    gender:'male'
}*/
```

