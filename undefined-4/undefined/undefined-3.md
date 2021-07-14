# 심볼

## property key : 문자형

```javascript
const obj = {
    1 : '1입니다',
    false : '거짓'
}
Object.keys(obj); // [ "1","false"]
obj['1'] //1입니다
obj['false'] //
```

## property key :  

```javascript
const id = Symbol('id');
const user = {
    name : 'mike',
    age : 30,
    [id] : 'myid'
}
Object.keys(user); //["name","age"]
```

## Symbol : 유일성  보장  

```javascript
//생긴거는 같지만 다르다고 나옴.
const a = symbol();// new를 붙이지 않는다.
const b = symbol();

console.log(a);
console.log(b);

a === b ; //false
a == b ; //false
```

## symbol for\(\) : 전역심볼  

하나의 심볼만 보장받을 수 있음 없으면 만들고, 있으면 가져오기 때문  
symbol함수는 매번 다른 symbol값을 생성하지만, symbol.for 메소드는 하나를 생성한 뒤 키를 통해 같은 symbol을 공유  


## description

전역심볼이 아닌 심볼은 keyfor을 사용 할수 없고 description을 사용해야함.

### getonepropertysymbols\(user\) 숨겨진 Symbol key 보는 법 

  


```javascript
// 다른 개발자가 만들어 놓은 객체
const user = {
    name: 'mike',
    age:30
};

//내가 작업
//user.showName = function (){}
const showName = Symbol('show name');
user[showName] = function(){
    console.log(this.name);
};

user[showName]();

//사용자가 접속하면 보는 메세지
for(let key in user){
    console.log(`His ${key} is ${user[key]}.`);
}
```

