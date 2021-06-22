# Flexbox Image Gallery

![](../.gitbook/assets/image%20%2827%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <div class="panels">
      <div class="panel panel1">
        <p>hey</p>
        <p>Let's</p>
        <p>Dance</p>
      </div>
      <div class="panel panel2">
        <p>Give</p>
        <p>Take</p>
        <p>Receive</p>
      </div>
      <div class="panel panel3">
        <p>Experience</p>
        <p>It</p>
        <p>Today</p>
      </div>
      <div class="panel panel4">
        <p>Give</p>
        <p>All</p>
        <p>You Can</p>
      </div>
      <div class="panel panel5">
        <p>Life</p>
        <p>In</p>
        <p>Motion</p>
      </div>
    </div>
```
{% endtab %}

{% tab title="CSS" %}
```css
      html {
        box-sizing: border-box;
        background: #ffc600;
        font-size: 20px;
        font-weight: 200;
      }
      body {
        margin: 0;
      }
      *,
      *:before,
      *:after {
        box-sizing: inherit;
      }
      .panels {
        min-height: 100vh;
        overflow: hidden;
        display: flex;
      }
      .panel {
        background: #6b0f9c;
        box-shadow: inset 0 0 0 5px rgba(255, 255, 255, 0.1);
        color: white;
        text-align: center;
        align-items: center;
        transition: font-size 0.7s cubic-bezier(0.61, -0.19, 0.7, -0.11),
          flex 0.7s cubic-bezier(0.61, -0.19, 0.7, -0.11), background 0.2s;
        font-size: 20px;
        background-size: cover;
        background-position: center;
        flex: 1;
        justify-content: center;
        align-items: center;
        display: flex;
        flex-direction: column;
      }
      .panel1 {
        background-image: url(https://images.unsplash.com/photo-1586879542102-18fd21fb46fa?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=668&q=80);
      }
      .panel2 {
        background-image: url(https://images.unsplash.com/photo-1621496503717-095a410e1566?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=668&q=80);
      }
      .panel3 {
        background-image: url(https://images.unsplash.com/photo-1618327146795-3de30b405e4f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=668&q=80);
      }
      .panel4 {
        background-image: url(https://images.unsplash.com/photo-1607736224736-3126ffedbff4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=668&q=80);
      }
      .panel5 {
        background-image: url(https://images.unsplash.com/photo-1623140922112-9cfc0e71b8fc?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2468&q=80);
      }

      .panel > * {
        margin: 0;
        width: 100%;
        transition: transform 0.5s;
        flex: 1 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      .panel > *:first-child {
        transform: translateY(-100%);
      }
      .panel.open-active > *:first-child {
        transform: translateY(0);
      }
      .panel > *:last-child {
        transform: translateY(100%);
      }
      .panel.open-active > *:last-child {
        transform: translateY(0);
      }
      .panel {
        text-transform: uppercase;
        text-shadow: 0 0 4px rgba(0, 0, 0, 0.72), 0 0 14px rgba(0, 0, 0, 0.45);
        font-size: 2em;
      }
      .panel p:nth-child(2) {
        font-size: 4em;
      }
      .panel.open {
        font-size: 40px;
        flex:5;
      }
      .cta {
        color: #fff;
        text-decoration: none;
      }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
        const panels = document.querySelectorAll('.panel');

        function toggleOpen(){
            console.log('hello');
            this.classList.toggle('open');
        }

        function toggleActive(e){
            console.log(e.propertyName);
            if(e.propertyName.includes('flex')){
                this.classList.toggle('open-active');
            }
        }

        panels.forEach(panel => panel.addEventListener('click',toggleOpen));
        panels.forEach(panel => panel.addEventListener('transitionend',toggleActive));
        
```
{% endtab %}
{% endtabs %}

