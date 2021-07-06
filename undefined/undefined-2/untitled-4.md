# 12. Promise



```javascript
// 1. Producer
// promise를 만드는 순간 executer가 바로 실행된다.
 const  promise = new promoise((resolve, reject) => {
  //doing some heavy work (network , read files )
   console.log('doing something');
   setTimeout(()=> { 
//      resolve('ellie')
   reject(new Error('no network'));
   }, 2000 );
  });
  
  // 2.Consumers : then, catch, finally
promise
  .then(value  =>{
  console.log(value);
}); //ellie
  .catch(error => {
  console.log(error);
 }); //no network
  .finally(() => {
  console.log('finally')
  }); //성공/실패와 상관없이 마지막에 무조건 실행한다.
 
  
  
  // 3.Promise chaining
const fetchNumber = new Promise((resolve,reject)=>{
  setTimeOut(()=>resolve(1),1000);  // 1
});
fetchNumber
  .then(num=>num*2) //2
  .then(num=>num*3) //6
  .then(num=>{
    return new Promise((resolve,reject)=>{
    setTimeout(()=>resolve(num-1),1000);  //1
  });
})
.then(num => console.log(num)); //2초  5

// 4. Error handling
const getHen = () =>
  new Promise((resolve,reject) => {
    setTimeout(()=>resolve('hen'),1000);
  });
const getEgg = hen =>
  new Promise((resolve,reject) => {
    setTimeout(()=>resolve(`${hen}=>egg`),1000);
  });
const cook = egg =>
  new Promise((resolve,reject) => {
    setTimeout(()=>resolve(`${egg}=>fried egg`),1000);
  }); 
getHen()
  .then(getEgg)
  .then(cook)
  .then(console.log)
  .catch(console.log)
```

