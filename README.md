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

