# 모듈

{% hint style="info" %}
모듈 은 부품이라고 이해하면 됨.  
다른프로그램에서 모듈화 하는 기법.  
  
자바스크립트가 구동되는 환경을 호스트환경 이라고함.
{% endhint %}

  
별도의 파일로 분류해서 호출할수 있음.

{% tabs %}
{% tab title="모듈.html" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <script src="greeting.js"></script>
    <title>Document</title>
</head>
<body>
    <script>
        alert(welcome());
    </script>
</body>
</html>
```
{% endtab %}

{% tab title="greeting.js" %}
```javascript
function welcome(){
    return 'hello'
}
```
{% endtab %}
{% endtabs %}

  
node.js \(영상참조\)  


라이브러\(jQuery같\)

