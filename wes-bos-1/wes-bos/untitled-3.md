# HTML5 Canvas

![](../../.gitbook/assets/image%20%2827%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
<canvas id="draw" width="800" height="800"></canvas>
```
{% endtab %}

{% tab title="CSS" %}
```css
        html, body {
            margin:0;
        }
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
        const canvas = document.querySelector('#draw');
        const ctx = canvas.getContext('2d');
        canvas.width= window.innerWidth;
        canvas.height= window.innerHeight;
        ctx.strokeStyle = '#bada55';
        ctx.lineJoin = 'round';
        ctx.lineCap = 'round';
        ctx.lineWidth = 100;
        // ctx.globalCompositeOperation = 'multiply';

        let isDrawing = false;
        let lastX = 0;
        let lastY = 0;
        let hue = 0;
        let direction = true;

        function draw(e){
            if(!isDrawing) return;
            console.log(e);
            ctx.strokeStyle = `hsl(${hue}, 100%, 50%)`;
            ctx.beginPath();
            //start from
            ctx.moveTo(lastX,lastY);
            //go to
            ctx.lineTo(e.offsetX,e.offsetY);
            ctx.stroke();
            [lastX, lastY] = [e.offsetX, e.offsetY];

            hue++;
            if(hue >= 360){
                hue = 0
            }
        }
        if(ctx.lineWith >= 500 || ctx.lineWidth <= 1){
            direction = !direction;
        }
        if(direction){
            ctx.lineWidth++;
        } else {
            ctx.lineWidth--;   
        }


        canvas.addEventListener('mousedown',(e) => {
            isDrawing = true;
            [lastX, lastY] = [e.offsetX, e.offsetY];
        });

        canvas.addEventListener('mousemove',draw);
        canvas.addEventListener('mouseup',() => isDrawing = false);
        canvas.addEventListener('mouseout',() => isDrawing = false);
```
{% endtab %}
{% endtabs %}

