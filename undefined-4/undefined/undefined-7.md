# 상속, 프로토타입

```javascript
 const bmw = {
  color:"red",
  wheels : 4,
  navigation:1,
  drive(){
    console.log('drive..');
  },
};

const benz = {
  color: "black",
  wheels : 4,
  navigation:1,
  drive(){
    console.log('drive..');
  },
};

const audi = {
  color: "blue",
  wheels : 4,
  navigation:1,
  drive(){
    console.log('drive..');
  },
};
//여기서 똑같이 반복되는 부분을 묶어줌.
const car = {
  color:"red",
  wheels : 4,
  navigation:1,
  drive(){
    console.log('drive..');
  },
};


 const bmw = {
  color:"red",
};

const benz = {
  color: "black",
};

const audi = {
  color: "blue",
};
bmw.__proto__ = car;
benz.__proto__ = car;
audi.__proto__ = car;
//이러면 car가 bmw,benz,audi의 프로토타입이 되는 것.

const x5 = {
  color:"white",
  nameL"x5",
};
x5.__proto__ = bmw;
//이런식으로 계속 상속가능.
```



