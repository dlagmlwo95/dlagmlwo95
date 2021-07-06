# 노드의 변경

## 노드추가

{% hint style="info" %}
document.createElement\(tagname\) 엘리먼트 노드를 추가한다.  
document.createTextNode\(data\) 텍스트 노드를 추가한다.

appendChild\(child\) 노드의 마지막 자식으로 주어진 엘리먼트 추가  
insertBefore\(newElement, referenceElement\) 두번째 인자로 엘리먼트를 전달 했을 때 이것 앞에 엘리먼트가 추가된다.
{% endhint %}



```markup
<ul id="target">
    <li>HTML</li>
    <li>CSS</li>
</ul>
<input type="button" onclick="callAppendChild();" value="appendChild()" />
<input type="button" onclick="callInsertBefore();" value="insertBefore()" />
<script>
    function callAppendChild(){
        var target = document.getElementById('target');
        var li = document.createElement('li');
        var text = document.createTextNode('JavaScript');
        li.appendChild(text);
        target.appendChild(li);
    }
    // 결과 HTML CSS Javascript 로 나옴
 -------------------------------------------------------
    function callInsertBefore(){
        var target = document.getElementById('target');
        var li = document.createElement('li');
        var text = document.createTextNode('jQuery');
        li.appendChild(text);
        target.insertBefore(li, target.firstChild); //중간에 넣기.
    }
    // 결과 jQuery HTML CSS 순으로 나옴
</script>
```

## 노드 제거,바꾸

{% hint style="info" %}
removeChild\(child\) 엘리먼트 노드를 제거한다.  
replaceChild\(newChild, oldChild\)  엘리먼트 노드를 바꾼다.
{% endhint %}



