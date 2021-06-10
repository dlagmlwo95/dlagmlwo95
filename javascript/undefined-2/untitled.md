# Untitled

HTML : 정보  
CSS : 디자인  
JAVASCRIPT : 웹브라우저, HTML 제어



## inline

{% tabs %}
{% tab title="inline.html" %}
```markup
<body>
    <input type="button" value="Hello world" onclick="alert('Hello world')">
</body>
```
{% endtab %}
{% endtabs %}

## script / 외부 파일로 분리 

{% tabs %}
{% tab title="script.html" %}
```markup
    <input type="button" id="hw" value="Hello world" />
    <script src="script.js"></script>
    //script 태그를 써야 유지보수나 정보를 제어하기 편함.
```
{% endtab %}

{% tab title="script.js" %}
```javascript
var hw = document.getElementById('hw');
hw.addEventListener('click', function(){
    alert('Hello world');
})
```
{% endtab %}
{% endtabs %}

## Script 파일의 위

{% tabs %}
{% tab title="script.html" %}
```markup
<!DOCTYPE html>
<html>
<head>
    <script src="script.js"></script>
</head>
<body>
    <input type="button" id="hw" value="Hello world" />
</body>
</html>
```
{% endtab %}

{% tab title="script.js" %}
```javascript
window.onload = function(){
    var hw = document.getElementById('hw');
    hw.addEventListener('click', function(){
        alert('Hello world');
    })
}
//onload 모든코드가 모두 읽혔을 때 함수를 실행시켜
```
{% endtab %}
{% endtabs %}

