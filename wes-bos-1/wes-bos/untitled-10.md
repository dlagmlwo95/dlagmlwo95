# Follow Along Links

![](../../.gitbook/assets/image%20%2832%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <nav>
      <ul class="menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">Order Status</a></li>
        <li><a href="#">Tweets</a></li>
        <li><a href="#">Read Our History</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </nav>
    <div class="wrapper">
      <p>
        Lorem ipsum is a <a href="#">placeholder</a> text commonly used to
        demonstrate the visual form of a <a href="#">document</a> or a typeface
        <a href="#">without</a> relying on meaningful content.
      </p>
      <p>
        Lorem ipsum may be <a href="#">used as a placeholder</a> before final
        copy is <a href="#">available.</a> It is also used to<a href="#">
          temporarily</a
        >
        replace text in a process called greeking,<a href="#"> which allows</a>
        designers to consider <a href="#">the</a> form of a webpage or
        <a href="#">publication,</a>
      </p>
      <p>
        without <a href="#">the meaning of</a> the text<a href="#">
          influencing</a
        >
        the design. Lorem ipsum is <a href="#">typically</a> a corrupted version
        of <a href="#">'De finibus bonorum et malorum',</a> a 1st century BC
        text by the Roman statesman and philosopher Cicero,
      </p>
    </div>

```
{% endtab %}

{% tab title="CSS" %}
```css
      body {
        min-height: 100vh;
        margin: 0;
        background: rgba(14, 11, 212, 0.575);
      }
      .wrapper {
        margin: 0 auto;
        max-width: 500px;
        font-size: 20px;
        line-height: 2;
        position: relative;
      }
      a {
        text-decoration: none;
        color: #000;
        background: rgba(0.0.0.05);
        border-radius: 20px;
      }
      ul,
      li {
        list-style: none;
      }
      .highlight {
        transition: all 0.2s;
        border-bottom: 2px solid #fff;
        position: absolute;
        top: 0;
        background: #fff;
        left: 0;
        z-index: -1;
        border-radius: 20px;
        display: block;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
      }
      .menu {
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
        margin: 0 auto;
      }
      .menu li a {
        display: inline-block;
        padding: 5px;
        margin: 0 20px;
        color: black;
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const triggers = document.querySelectorAll("a");
      const highlight = document.createElement("span");
      highlight.classList.add("highlight");
      document.body.append(highlight);

      function highlightLink() {
        const linkCoords = this.getBoundingClientRect();
        console.log(linkCoords);
        const coords = {
          width: linkCoords.width,
          height: linkCoords.height,
          top: linkCoords.top + window.scrollY,
          top: linkCoords.left + window.scrollX,
        };

        highlight.style.width = `${linkCoords.width}px`;
        highlight.style.height = `${linkCoords.height}px`;
        highlight.style.transform = `translate(${linkCoords.left}px, ${linkCoords.top}px)`;
      }
      triggers.forEach((a) => a.addEventListener("mouseenter", highlightLink));
```
{% endtab %}
{% endtabs %}

