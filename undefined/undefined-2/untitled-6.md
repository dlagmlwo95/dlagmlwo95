# 10.JSON

HTTP : hypertext transfer protocal

AJAX : 웹페이지에서 동적으로 서버에게 데이터를 주고 받을 수 있는 기술을 의미 대표적으로는 XHR가 있음.\(간단하게 데이터를 주고받을 수 있음.\)

XML 은 html과 같은 마크업 언어. XML은 사용하면 불필요한 태그들이 많이 들어가 JSON을 많이 사용한다.  
json은 javascript 처럼 key와 value로 이루져 있다.



## OBJECT -&gt; JSON 변환

```javascript
let json = JSON.stringify(true);
console.log(json); 

json = JSON.stringify(['apple','banana']);
console.log(json);

let rabbit ={ 
  name: 'tori',
  color: 'white',
  size : null,
  birthDate : new Date(),
  jump: () => {
    console.log(`${name} can jump!`)
  },
};
json = JSON.stringify(rabbit);
console.log(json);
//{"name":"tori","color":"white","size":null,"birthDate":"2021-07-06T09:55:55.822Z"}

// 이름만 출력
json = JSON.stringify(rabbit, ["name"]);
console.log(json); //{"name":"tori"}

//이름 변환
json = JSON.stringify(rabbit, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return key === 'name' ? 'ellie' : value;
});
console.log(json);
//{"name":"ellie"} 로 바뀜.

```

## JSON -&gt; OBJECT 변환

```javascript
json = JSON.stringify(rabbit);
console.log(json);
const obj = JSON.parse(json, (key, value) => {
    console.log(`key: ${key}, value: ${value}`);
    return key === 'birthDate' ? new Date(value) : value;
});
console.log(obj);
rabbit.jump();
// obj.jump();

console.log(rabbit.birthDate.getDate());
console.log(obj.birthDate.getDate());
```

