# 6강 : Component로 HTML 깔끔하게 줄이는 법

```jsx
/* eslint-disable */
import React, { useState } from "react";
import logo from "./logo.svg";
import "./App.css";

function App() {
  let [글제목, 글제목변경] = useState([
    "남자코트 추천",
    "강남 우동 맛집",
    "리액트",
  ]);
  let [따봉, 따봉변경] = useState(0);
  let posts = "강남 고기 맛집";

  // function 제목바꾸기 (){
  //   var newArray = [...글제목];
  //   newArray[0] = '여자코트 추천';
  //   글제목변경(newArray);
  // }

  return (
    <div className="App">
      <div className="black-nav">
        <div>개발 Blog</div>
      </div>
      {/* <button onClick={ 제목바꾸기 } >버튼</button> */}
      <div className="list">
        <h3>
          {글제목[0]}{" "}
          <span
            onClick={() => {
              따봉변경(따봉 + 1);
            }}
          >
            👍
          </span>
          {따봉}
        </h3>
        <p>2월 17일 발행</p>
        <hr />
      </div>
      <div className="list">
        <h3>{글제목[1]}</h3>
        <p>2월 18일 발행</p>
        <hr />
      </div>
      <div className="list">
        <h3>{글제목[2]}</h3>
        <p>2월 19일 발행</p>
        <hr />
      </div>

      <Modal />
      
    </div>
  );
}

function Modal() {
  return (
    <>
      <div className="modal">
        <h2>제목</h2>
        <p>날짜</p>
        <p>상세내용</p>
      </div>
    </>
  );
}

export default App;

```



Component 유의사항   
1.이름은 대괄호  
2. return\(\)안에 있는건 로 묶거나 &lt;&gt; &lt;/&gt; 로 묶어야함

Component 장점 : 관리가 편해짐 

Component 단점 : state 쓸 때 복잡해짐. Component로 바꾸면 좋은 것

* 반복출현하는 HTML덩어리
* 자주 변경되는 HTML UI
* 다른 페이지 만들때 컨퍼넌트로 만듬

