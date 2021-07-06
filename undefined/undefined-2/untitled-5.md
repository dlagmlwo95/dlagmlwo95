# 11. 비동기, Call back

자바스크립트의 비동기 처리  
callback  
promise   
async / await

hosting : 변수와 함수선언들이 자동적으로 제일 위로 올라가는 것.



## 동기 Synchronous Callback

정해진 순서에 맞게 

## 비동기 Asynchronous callback

언제실행될지 모름

## 동기 / 비동기

```javascript
console.log('1');
setTimeout(() => console.log('2'),1000);
console.log('3');
// 동기
function printImmediately(print){
  print();
}

// 비동기
function printWithDelay(print, timeout){
    setTimeout(print, timeout);
}
console.log('1');  //동기
setTimeout(() => console.log('2'),1000); //비동기
console.log('3'); //동기
printImmediately(() => console.log('hello')); //
printWithDelay(() => console.log('async callback'),2000); //
// 1 3 hello 2 asynccallback
```



## 콜백지옥

1.가독성 떨어짐  
2.유지보수가 어려움   
3.promise로 해결한다.



```javascript
class UserStorage {
  loginUser(id, password, onSuccess, onError){
    setTimeout(() => {
      if(
        (id === 'ellie' && password === 'dream"' ||
        (id === 'coder' && password === 'academy')
      ) {
        onSuccess(id);
      }else {
        onError(new Error('not found'));
      }
    }, 2000);
  }
  
  getRoles(user, onSuccess, onError) {
    setTimeout(() => {
      if(user === 'ellie') {
        onSuccess({name: 'ellie', role: 'admin'});
      } else {
        onError(new Error('no access'));
      }
    }, 1000)
  }
}

const userStorage = new UserStorage();
const id = prompt('enter your id');
const password = prompt('enter your password');
userStorage.loginUser(
  id,
  password,
  user => {
    uwerStorage.getRoles(user,
    userWithRole => {
      alert(`hello ${user.name}, you have a ${user.role} role`)
    },
    error => {
      console.log(error)
    });
  },
  error => {console.log(error)}
};
```



