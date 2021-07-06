# 13. async, await

async, await은 promise를 좀더 간결하고 동기적으로 보여준다

## async

```javascript
//앞에 async라는 코드를 작성한다.
async function fetchUser() {
  // do network reqeust in 10 secs....
  return 'ellie';
}

const user = fetchUser();
user.then(console.log);
console.log(user);
```

## await

```javascript
//async 함수에서만 사용 
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function getApple() {
  await delay(3000); 
  return 'apple';
}

async function getBanana() {
  await delay(3000); 
  return 'banana';
}

async function pickFruits() {
  const applePromise = getApple();
  const bananaPromise = getBanana();
  const apple = await applePromise;
  const banana = await bananaPromise;
  return `${apple} + ${banana}`;
}
pickFruits().then(console.log);

// 3.useful Promis APIs
function pickAllFruits() {
  return Promise.all([getApple(), getBanana()]).then(fruits =>
    fruits.join(' + ')
  );
}
pickAllFruits().then(console.log);
```

