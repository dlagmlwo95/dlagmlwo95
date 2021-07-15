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
    function(err){}        //
);
```

