# Checkbox Challenge

![](../.gitbook/assets/image%20%2829%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <div class="inbox">
        <div class="item">
            <input type="checkbox">
            <p>This is an inbox layout.</p>
        </div>
        <div class="item">
            <input type="checkbox">
            <p>Chek one item</p>
        </div>
        <div class="item">
            <input type="checkbox">
            <p>Hold down your Shift key</p>
        </div>
        <div class="item">
            <input type="checkbox">
            <p>Check a lower item</p>
        </div>
        <div class="item">
            <input type="checkbox">
            <p>Try do it with out any libraies</p>
        </div>
    </div>

```
{% endtab %}

{% tab title="CSS" %}
```css
    html {
      background:#2765da;
    }

    .inbox {
      width:400px;
      margin:100px auto;
      background:white;
      
    }

    .item {
      display:flex;
      align-items:center;
      border-bottom: 1px solid #dedede;
    }

    .item:last-child {
      border-bottom:0;
    }


    input:checked + p {
      background:#fcf2f2;
      text-decoration: line-through;
    }

    input[type="checkbox"] {
      margin:20px;
    }

    p {
      margin:0;
      padding:20px;
      font-size: 20px;
      font-weight: 200;
      border-left: 1px solid #ffd1d1;
    }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const checkboxes = document.querySelectorAll('.inbox input[type="checkbox"]');
      
      let lastChecked;

      function handlecheck(e){
        if(e.shiftKey && this.checked){
          let inBetween = false;
          if (e.shiftKey && this.checked){
            checkboxes.forEach(checkbox => {
              console.log(checkbox);
              if (checkbox === this || checkbox === lastChecked){
                inBetween = !inBetween;
                console.log('starting to check them inbetween')
              }
              if(inBetween){
                checkbo.checked = true;
              }
            })
          }
        }
        lastChecked = this;
      }

      

      checkboxes.forEach(checkbox => checkbox.addEventListener('click',handlecheck));
```
{% endtab %}
{% endtabs %}

