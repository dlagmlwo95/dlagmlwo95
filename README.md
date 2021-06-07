# Node.js

1.Node.js 설치하기  
[https://nodejs.org/en](https://nodejs.org/en/)  
  
명령프롬프트 -&gt; dir desktop - \(주소에서 설치 후\) node -v로 설치 되어있는지 확인 -&gt; npx create-react-app react5000 쳐서 나머지 설치





2. 기본 개념 익히기  
2-1 출력하  
 \(index.js\)

```javascript
import React from 'react';
import ReactDOM from 'react-dom';


ReactDOM.render(<h1>hello</h1>,document.getElementById('root'));
```

2-2 JSX  
보는법 : 터미널에 npm start 검색.  
\(1,2 같음\)

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const name = "imheejae"
const hello = <h1>hello{name}</h1>

ReactDOM.render(hello,document.getElementById('root'));
```

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

function helloName(name){
  return name.nick;
}

const name = {
  nick : "imheejae",
}

const hello = <h1>hello, {helloName(name)}</h1>

ReactDOM.render(hello,document.getElementById('root'));
```

2-3 렌더링

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

//렌더링

function clock(){
  const element = (
    <div>
      <h1>hello, imheejae</h1>
      <h2>지금은 {new Date().toLocaleTimeString()}입니다.</h2>
    </div>
  );
  ReactDOM.render(element,document.getElementById('root'));
}
setInterval(clock, 1000);   //서클이라는 함수를 1초에 한번씩 진행시켜라.


/* 자바스크립트
let clock = document.getElementById("clock");

        setInterval(function() {
            clock.innerHTML = new Date().toLocaleTimeString();
        }, 1000);
*/
```

2-4 컨퍼넌트\(중요\) 

```javascript
import React from 'react';
import reactDom from 'react-dom';

//컨퍼넌트는 앞에를 대문자로 씀(Hello) 함수는 소문자
function Hello(){
  return <h1>Hello, imheejae</h1>
}

const element = <Hello />; //컨퍼넌트 사용법

reactDom.render(element, document.getElementById('root'));

// SPA : 싱글페이지
```

```jsx
props 추가

function Hello(props){
  return <h1>Hello,{props.name}</h1>
}

const element = <Hello name = "imheejae" />;

reactDom.render(element, document.getElementById('root'));

```

로우터 설치하

```jsx
//로우터 설치하기 
npm install react-router-dom
```

```jsx
//sass 설치하기
npm install node-sass
npm install node-sass@4.14.1
```



```jsx
import React from 'react';
import Main from './components/pages/Main';
import About from './components/pages/About';
import Reference from './components/pages/Reference';
import Script from './components/pages/Script';
import Youtube from './components/pages/Youtube';
import Contact from './components/pages/Contact';
import Portfolio from './components/pages/Portfolio';
import {BrowserRouter as Router, Route } from 'react-router-dom';

function App(){
  return (
    <Router>
      <Route path="/" exact component={Main} />
      <Route path="/about" exact component={About} />
      <Route path="/reference" exact component={Reference} />
      <Route path="/script" exact component={Script} />
      <Route path="/youtube" exact component={Youtube} />
      <Route path="/contact" exact component={Contact} />
      <Route path="/portfolio" exact component={Portfolio} />
    </Router>
  )
}

export default App;




폴(About.js)

import React from 'react';

function About(){
    return <div>about 페이지입니다.</div>
}

export default About;
```







sass 는 이름명 앞에 _가 붙음 ex\)_ \_layout.scss  
  
index.js 에 import './index.scss'; 넣어준다.

```jsx
index.scss

@charset "UTF-8";

//Base
@import "./assets/styles/fonts";
@import "./assets/styles/base";

//layout
@import "./assets/styles/layout";

//page
@import "./assets/styles/pages";

//Loading
@import "./assets/styles/loader";

----------------------------------------------
각 폴더 이름은 앞에 _ 붙이
```

