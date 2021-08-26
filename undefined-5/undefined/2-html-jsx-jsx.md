# 2강 리액트에선 HTML대신 JSX 써야함 \(JSX 사용법\)

{% tabs %}
{% tab title="React JSX" %}
```jsx
import logo from './logo.svg';
import './App.css';

function App() {
  
  let posts = '강남 고기 맛집';
  function 함수(){
    return 100
  }
  

  return (
    <div className="App">
      <div className="black-nav">
        <div style={ { color : 'blue' , fontSize : '30px'} }>개발 Blog</div>
      </div>
      <h4> { posts }</h4>
    </div>
  );
}

export default App;

```
{% endtab %}

{% tab title="css" %}
```css
body {
  font-family: 'nanumsquare';
}
.black-nav {
  background:#000;
  width:100%;
  display:flex;
  color:#fff;
  padding:20px;
  font-weight:6600;
  font-size:20px;
}
```
{% endtab %}
{% endtabs %}



