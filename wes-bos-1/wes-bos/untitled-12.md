# Array Reduce Works

![](../../.gitbook/assets/image%20%2833%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
    <ul class="video">
        <li data-time="1:56">
            Video 1
        </li>
        <li data-time="6:16">
            Video 2
        </li>
        <li data-time="1:24">
            Video 3
        </li>
        <li data-time="5:30">
            Video 4
        </li>
        <li data-time="1:04">
            Video 5
        </li>
        <li data-time="8:21">
            Video 6
        </li>
        <li data-time="4:06">
            Video 7
        </li>
        <li data-time="3:40">
            Video 8
        </li>
        <li data-time="12:42">
            Video 91
        </li>
        <li data-time="2:14">
            Video 10
        </li>
        <li data-time="9:2">
            Video 11
        </li>
    </ul>
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
        const timeNodes = Array.from(document.querySelectorAll('[data-time]'));

        const seconds = timeNodes
        .map(node => node.dataset.time)
        .map(timeCode => {
            const [mins, secs] = timeCode.split(':').map(parseFloat);
            return (mins * 60) + secs;
        })
        .reduce((total, vidSeconds) => total + vidSeconds);

        let secondsLeft = seconds;
        const hours = Math.floor(secondsLeft / 3600);
        secondsLeft = secondsLeft % 3600;
        const mins = Math.floor(secondsLeft / 60);
        secondsLeft = secondsLeft % 60;

        document.write(hours+':' , mins+':', secondsLeft);
        
```
{% endtab %}
{% endtabs %}

