# Drag to Scroll

![](../.gitbook/assets/image%20%2834%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <div class="items">
      <div class="item item1">01</div>
      <div class="item item2">02</div>
      <div class="item item3">03</div>
      <div class="item item4">04</div>
      <div class="item item5">05</div>
      <div class="item item6">06</div>
      <div class="item item7">07</div>
    </div>

```
{% endtab %}

{% tab title="CSS" %}
```css
      html {
        box-sizing: border-box;
        background: #999;
        background-size: cover;
      }
      *,
      *:before,
      *:after {
        box-sizing: inherit;
      }

      body {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
        margin: 0;
      }

      .items {
        height: 800px;
        padding: 100px;
        width: 100%;
        border: 1px solid white;
        box-shadow: 0 0 10px 7px rgba(0, 0, 0, 0.09);
        overflow-x: scroll;
        overflow-y: hidden;
        white-space: nowrap;
        user-select: none;
        cursor: pointer;
        transition: all 0.2s;
        transform: scale(0.98);
        will-change: transform;
        position: relative;
        background: rgba(255, 255, 255, 0.1);
        font-size: 0;
        perspective: 500px;
      }

      .items.active {
        background: rgba(255, 255, 255, 0.3);
        cursor: grabbing;
        transform: scale(1);
      }
      .item {
        width: 200px;
        height: calc(100% - 40px);
        display: inline-flex;
        align-items: center;
        justify-content: center;
        font-size: 80px;
        font-weight: 100;
      }
      .item1 {
        background: red;
      }
      .item2 {
        background: orange;
      }
      .item3 {
        background: yellow;
      }
      .item4 {
        background: green;
      }
      .item5 {
        background: skyblue;
      }
      .item6 {
        background: blue;
      }
      .item7 {
        background: violet;
      }

      .item:nth-child(even) {
        transform: scaleX(1.5) rotateY(45deg);
      }
      .item:nth-child(odd) {
        transform: scaleX(1.5) rotateY(-45deg);
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const slider = document.querySelector(".items");
      let isDown = false;
      let startX;
      let scrollLeft;
      slider.addEventListener("mousedown", (e) => {
        isDown = true;
        slider.classList.add("active");
        startX = e.pageX - slider.offsetLeft;
        scrollLeft = slider.scrollLeft;
        console.log(scrollLeft);
      });
      slider.addEventListener("mouseleave", () => {
        isDown = false;
        slider.classList.remove("active");
      });
      slider.addEventListener("mouseup", () => {
        isDown = false;
        slider.classList.remove("active");
      });
      slider.addEventListener("mousemove", (e) => {
        if (!isDown) return; //stop running it;
        e.preventDefault();
        let x = e.pageX - slider.offsetLeft;
        let walk = (x - startX) * 3;
        slider.scrollLeft = scrollLeft - walk;
      });
```
{% endtab %}
{% endtabs %}

