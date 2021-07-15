# async, await

## async

```javascript
//항상 promise로 
async function getName(){
  // return Promise.resolve('t');
  throw new Error('err..');
}
getName().catch((err) => {
  console.log(err);
});
```

## await

async함수 내부에서만 사용할수 있다

```javascript
function getName(name){
  return new Promise((resolve,reject) => {
    setTimeout(() => {
      resolve(name);
    },1000);
  });
}
async function showName(){
  const result = await getName('m');
  console.log(result);
}
console.log('시작')
showName()  //1

//예제 promise파일에 있음.
```

