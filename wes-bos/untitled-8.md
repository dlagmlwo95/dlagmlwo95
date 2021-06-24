# Dropdown Navigation

![](../.gitbook/assets/image%20%2835%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <h2>cool</h2>
    <nav class="top">
      <div class="dropdownBackground">
        <span class="arrow"></span>
      </div>

      <ul class="cool">
        <li>
          <a href="#">About Me</a>
          <div class="dropdown dropdown1">
            <div class="bio">
              <img src="http://logo.clearbit.com/wesbos.com" />
              <p>
                orem ipsum is a placeholder text commonly used to demonstrate
                the visual form of a document or a typeface without relying on
                meaningful content.
              </p>
            </div>
          </div>
        </li>

        <li>
          <a href="#">Courses</a>
          <ul class="dropdown courses">
            <li>
              <span class="code">REB</span>
              <a href="#">React For Beginners</a>
            </li>
            <li>
              <span class="code">ES6</span>
              <a href="#">ES6 FOR EVERYONE</a>
            </li>
            <li>
              <span class="code">HTML</span>
              <a href="#">HTML EVERYONE</a>
            </li>
            <li>
              <span class="code">CSS</span>
              <a href="#">JAVASCRIPT</a>
            </li>
          </ul>
        </li>
        <li>
          <a href="#">Other Links</a>
          <ul class="dropdown dropdown3">
            <li><a href="button" href="#">Twitter</a></li>
            <li><a href="button" href="#">Facebook</a></li>
            <li><a href="button" href="#">Youtube</a></li>
          </ul>
        </li>
      </ul>
    </nav>

```
{% endtab %}

{% tab title="CSS" %}
```css
      html {
        box-sizing: border-box;
      }
      *,
      *::before,
      *:after {
        box-sizing: inherit;
      }
      body {
        min-height: 100vh;
        background: #999;
      }
      nav {
        position: relative;
        perspective: 600px;
      }
      .cool > li > a {
        color: yellow;
        text-decoration: none;
        font-size: 20px;
        background: rgba(0, 0, 0, 0.2);
        padding: 10px 20px;
        display: inline-block;
        margin: 20px;
        border-radius: 5px;
      }

      nav ul {
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
      }
      .cool > li {
        position: relative;
        display: flex;
        justify-content: center;
      }
      .dropdown {
        opacity: 0;
        position: absolute;
        overflow: hidden;
        padding: 20px;
        top: -20px;
        border-radius: 2px;
        transition: all 0.5s;
        transform: translateY(100px);
        display: none;
      }
      .trigger-enter .dropdown {
        display: block;
      }
      .trigger-enter-active .dropdown {
        opacity: 1;
      }
      .dropdownBackground {
        width: 100px;
        height: 100px;
        position: absolute;
        background: #fff;
        border-radius: 4px;
        box-shadow: 0 50px 100px rgba(50, 50, 93, 0.1),
          0 15px 35px rgba(50, 50, 93, 0.15), 0 5px 15px rgba(0, 0, 0, 0.1);
        transition: all 0.3s, opacity 0.1s, translate 0.2s;
        transform-origin: 50% 0%;
        display: flex;
        justify-content: center;
        opacity: 0;
      }
      .dropdownBackground.open {
        opacity: 1;
      }
      .arrow {
        position: absolute;
        width: 20px;
        height: 20px;
        display: block;
        background: #fff;
        transform: translateY(-50%) rotate(45deg);
      }

      .bio {
        min-width: 500px;
        display: flex;
        justify-content: center;
        align-items: center;
        line-height: 1.7;
      }
      .bio img {
        float: left;
        margin-right: 20px;
      }
      .courses {
        min-width: 300px;
      }
      .courses li {
        padding: 10px 0;
        display: block;
        border-bottom: 1px solid rgba(0, 0, 0, 0.2);
      }
      .dropdown a {
        text-decoration: none;
        color: #ffc600;
      }
      a.button {
        background: black;
        display: block;
        padding: 10px;
        color: #fff;
        margin-bottom: 10px;
      }

      .button[href*="Twitter"] {
        background: #019fe9;
      }
      .button[href*="Facebook"] {
        background: #385998;
      }
      .button[href*="Youtube"] {
        background: red;
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const triggers = document.querySelectorAll(".cool > li");
      const background = document.querySelector(".dropdownBackground");
      const nav = document.querySelector(".top");

      function handleEnter() {
        this.classList.add("trigger-enter");
        //글씨와 흰박스 뜨는 시간
        setTimeout(
          () =>
            this.classList.contains("trigger-enter") &&
            this.classList.add("trigger-enter-active"),
          150
        );

        background.classList.add("open");

        const dropdown = this.querySelector(".dropdown");
        // 흰박스
        const dropdownCoords = dropdown.getBoundingClientRect();
        const navCoords = nav.getBoundingClientRect();

        //흰박스위치
        const coords = {
          height: dropdownCoords.height,
          width: dropdownCoords.width,
          top: dropdownCoords.top - navCoords.top,
          left: dropdownCoords.left - navCoords.left,
        };

        background.style.setProperty("width", `${coords.width}px`);
        background.style.setProperty("height", `${coords.height}px`);
        background.style.setProperty(
          "transform",
          `translate(${coords.left}px,${coords.top}px`
        );
      }
      function handleLeave() {
        this.classList.remove("trigger-enter", "trigger-enter-active");
        background.classList.remove("open");
      }

      triggers.forEach((trigger) =>
        trigger.addEventListener("mouseenter", handleEnter)
      );
      triggers.forEach((trigger) =>
        trigger.addEventListener("mouseleave", handleLeave)
      );
```
{% endtab %}
{% endtabs %}

