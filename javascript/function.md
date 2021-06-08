# 함수 function

{% hint style="info" %}
function 함수명 \( \[인자 ... \[,인자\]\]\) {  
                         코드  
                         return 반환값   
}
{% endhint %}

```javascript
        function numbering(){
            document.write(1);
        }
        numbering();  // 1
/**********************************************/
        function numbering(){
            i = 0;
            while(i < 10){
                document.write(i);
                i += 1;
            }
        }
        numbering();    //0123456789
```

