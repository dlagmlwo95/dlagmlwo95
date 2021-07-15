# Promise

### promise 사용법 

```javascript
const pr = new Promise((resolve,reject) => {});



const pr = new Promise((resolve,reject) => {
    seTimeout(()=>{
        resolve('ok')
    },3000)
});
//result는 undefined였다가 3초뒤에 ok가 됨.


const pr = new Promise((resolve,reject) => {
    seTimeout(()=>{
        reject(new Error('error..')
    },3000)
});
//pending(대기)였다가 3초뒤에 rejected가됨

```

### then을 이용해 resolve,reject를 처리할수잇다.

```javascript
pr.then(
    function(result){},   //이행되었을때실행
    function(err){}        //
);


const pr = new Promise((resolve,reject) => {
    seTimeout(()=>{
        resolve('ok')
    },3000)
});
pr.then(
    function(result){
        console.log(result + '  가지러가자.');  //위에가 resolve이기때문에 이것만 
    },
    function(err){
        console.log('다시 ㅜ문해주세요');
    }
);
```

### catch

```javascript
pr.then(
    function(result){},   //이행되었을때실행
    function(err){}        //거부되었을때 실행
);
//밑에껄로 바꾸기  catch로  실행하면 가독성을 잡아줄수있음.
pr.then(
    function(result){}
).catch(
    function(err){}
).finally(
    function(){
        console.log('주문끝')
    }
)

```



```javascript
//콜백헬, 
const f1 = (callback) => {
  setTimeout(function(){
    console.log('1번 주문');
    callback();
  },1000);
};

const f2 = (callback) => {
  setTimeout(function(){
    console.log('2번 주문');
    callback();
  },2000);
};
const f3 = (callback) => {
  setTimeout(function(){
    console.log('3번 주문');
    callback();
  },1500);
};
console.log('시작')
f1(function(){
  f2(function(){
    f3(function(){
      console.log('끝');
    });
  });
});



////ㅔpromise체이닝 
const f1 = () => {
  return new Promise((res,rej) => {
    setTimeout(() => {
      res('1번주문');
    },1000)
  });
};

const f2 = (message) => {
  console.log(message);
  return new Promise((res,rej) => {
    setTimeout(() => {
      res('2번주문');
    },2000)
  });
};

const f3 = (message) => {
  console.log(message);
  return new Promise((res,rej) => {
    setTimeout(() => {
      res('3번주문');
    },1500)
  });
};

console.loe('시작');
f1()
  .then((res) => f2(res))
  .then((res) => f3(res))
  .then((res) => console.log(res))
  .catch(console.log)
  .finally(() => {
    console.log('끝');
  });
  
//promise.all 한번에실행  모든작업이 될때까지 기다림.
//promise.race 하나라도 끝나면 끝.
Promise.all([f1(),f2(),f3()]).then((res) =>{
  console.log(res);
  console.timeEnd('x');
});
```

