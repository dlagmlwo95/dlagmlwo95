# Event Capture,Bubbling

## 버블링

  
한 요소에 이벤트가 발생하면, 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작합니다.가장 최상단의 조상 요소를 만날 때까지 이 과정이 반복되면서 요소 각각에 할당된 핸들러가 동작합니다.

{% tabs %}
{% tab title="HTML" %}
```markup
  <body class="body">
    <div class="one">
      <div class="two">
        <div class="three"></div>
      </div>
    </div>
    <button></button>
```
{% endtab %}

{% tab title="CSS" %}
```css
      html {
        box-sizing: border-box;
      }
      div {
        width: 100%;
        padding: 100px;
      }
      .one {
        background: cornflowerblue;
      }
      .two {
        background: blue;
      }
      .three {
        background: blueviolet;
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const divs = document.querySelectorAll("div");
      const button = document.querySelector("button");
      function logText(e) {
        console.log(this.classList.value);
        // e.stopPropagation();
        // console.log(this);
      }

      divs.forEach((div) =>
        div.addEventListener("click", logText, {
          capture: true,
          once: true,
        })
      );

      button.addEventListener("click", () => {
        console.log("click!!");
      });
```
{% endtab %}
{% endtabs %}

[https://ko.javascript.info/bubbling-and-capturing](https://ko.javascript.info/bubbling-and-capturing)

