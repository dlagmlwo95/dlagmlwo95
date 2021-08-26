# 3강 리액트에선 변수말고 state 만들어 쓰랬죠 \(useState\)

### useState 사용법

1. {useState} 상단에 첨부  
2. useState\(데이터\)

### state

1. 변수 대신 쓰는 데이터 저장공간
2. useState\(\)를 이용해 만들어야함
3. 문자,숫자,array,object 다 저장가능

### state에 데이터를 저장해 놓는 이유

1. 웹이 app처럼 동작하게 만들고 싶어서
2. state는 변경되면 HTML이 자동으로 재렌더링 된다.

### 자주 바뀌는, 중요한 데이터는 변수말고 state로 저장해서 사용 

![](../../.gitbook/assets/image%20%2840%29.png)

```jsx
let [a,b] = useState('남자 코트 추천');

여기서 a는 남자코트추천이고 b는 남자코트추천을 바꿀 수 있는 코드

```

```jsx
import React, { useState } from 'react';
import logo from './logo.svg';
import './App.css';

function App() {
  
  var [a,b] = [10,100];


  let [글제목,글제목변경] = useState(['남자 코트 추천','강남 우동 맛집']);

  let posts = '강남 고기 맛집';

  return (
    <div className="App">
      <div className="black-nav">
        <div>개발 Blog</div>
      </div>
      <div className="list">
        <h3>{글제목[1]}</h3>
        <p>2월 17일 발행</p>
        <hr/>
      </div>
    </div>
  );
}

export default App;

```

