# Text 객체

![](../../../.gitbook/assets/image%20%286%29.png)

```markup
<p id="target1"><span>Hello world</span></p>
<p id="target2"><!--공백존재; firstchild는 공백.-->
    <span>Hello world</span>
</p>
<script>
var t1 = document.getElementById('target1').firstChild;
var t2 = document.getElementById('target2').firstChild;
 
console.log(t1.firstChild.nodeValue);
try{
    console.log(t2.firstChild.nodeValue);   
} catch(e){
    console.log(e);
}
console.log(t2.nextSibling.firstChild.nodeValue);
 
</script>
```

