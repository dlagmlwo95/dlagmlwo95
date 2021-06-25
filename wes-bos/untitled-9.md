# Event Capture

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



