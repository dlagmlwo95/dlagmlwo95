# inline

{% hint style="info" %}
inline 태그의 정해진 속성의 이름으로 값을 주는 방식으로 이벤트를 설치하는 것.  
this 는 자기 자신을 의미한다.
{% endhint %}

```javascript
<!--자기 자신을 참조하는 불편한 방법-->
<input type="button" id="target" onclick="alert('Hello world, '+document.getElementById('target').value);" value="button" />
<!--this를 통해서 간편하게 참조할 수 있다-->
<input type="button" onclick="alert('Hello world, '+this.value);" value="button" />
```

