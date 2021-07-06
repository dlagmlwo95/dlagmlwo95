# CSS Variables

![](../../.gitbook/assets/image%20%2824%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <h2>Update Css variables with <span class='h1'>JS</span></h2>

    <div class="controls">
        <label for="spacing">Spacing:</label>
        <input type="range" name="spacing" min="10" max="200" value="10" data-sizing="px">
        
        <label for="blur">Blur:</label>
        <input type="range" name="blur" min="0" max="25" value="10" data-sizing="px">
        
        <label for="base">Base Color</label>
        <input type="color" name="base" value="#ffc600">
     </div> 
    <img
      src="https://images.unsplash.com/photo-1496196614460-48988a57fccf?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2534&q=80"
    />
```
{% endtab %}

{% tab title="CSS" %}
```css
      :root {
        --base: #ffc600;
        --spacing: 10px;
        --blur: 10px;
      }
      img {
        padding: var(--spacing);
        background: var(--base);
        filter: blur(var(--blur));
        width:400px;
        height:400px;
      }
      .h1 {
        color: var(--base);
      }
      body {
        text-align: center;
      }
      body {
        background: #193549;
        color: white;
        font-family: "helvetica neue", sans-serif;
        font-weight: 100;
        font-size: 50px;
      }
      .controls {
        margin-bottom: 50px;
      }
      a {
        color: var(--base);
        text-decoration: none;
      }

      input {
        width: 100px;
      }
```
{% endtab %}

{% tab title="JAVASCIRPT" %}
```javascript
      const inputs = document.querySelectorAll('.controls input');

      function handleUpdate() {
        const suffix = this.dataset.sizing || "";
        document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
      }

      inputs.forEach(input => input.addEventListener('change', handleUpdate));
      inputs.forEach(input => input.addEventListener('mousevome', handleUpdate));
```
{% endtab %}
{% endtabs %}

