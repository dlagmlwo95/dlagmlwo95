# Mouse Move Effect

![](../../.gitbook/assets/image%20%2831%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <div class="hero">
      <h1>👍WOAH!</h1>
    </div>
```
{% endtab %}

{% tab title="CSS" %}
```css
      body {
        margin: 0;
        padding: 0;
      }
      .hero {
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }
      h1 {
        text-shadow: 10px 10px 0 rgba(0, 0, 0, 0.1);
        font-size: 100px;
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const hero = document.querySelector(".hero");
      const text = document.querySelector("h1");
      const walk = 200; //100px

      function shadow(e) {
          //console.log(x,y) .hero 의 왼쪽 위 모서리 0,0 
        const {offsetWidth : width,offsetHeight: height } = hero;
        let { offsetX: x, offsetY :y} = e;
        // if쪽에서 전체 왼쪽위가 0,0
        if(this !== e.target){
            x = x + e.target.offsetLeft;
            y = y + e.target.offsetTop;
        }

        //hero의 중간
        const xWalk = Math.round((x/ width * walk) - (walk / 2));
        const yWalk = Math.round((y/ height * walk) - (walk / 2));

        text.style.textShadow = `
        ${xWalk}px ${yWalk}px 0 rgba(255,0,255,0.7),
        ${xWalk * -1}px ${yWalk}px 0 rgba(0,255,255,0.7),
        ${yWalk}px ${xWalk * -1}px 0 rgba(0,255,0,0.7),
        ${yWalk * -1}px ${xWalk}px 0 rgba(0,0,255,0.7)
        `;

        
      }

      hero.addEventListener("mousemove", shadow);
```
{% endtab %}
{% endtabs %}

