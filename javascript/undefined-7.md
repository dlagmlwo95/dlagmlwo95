# 객체



{% hint style="info" %}
객체 { }
{% endhint %}

객체 만드는 

```javascript
1        var grades = {'egoing' : 10, 'kk8805' : 6, 'sorialgi':80};
        
2        var grades = {};
        grades['egoing'] = 10;
        grades['kk8805'] = 6;
        grades['sorialgi'] = 80;

3        var grades = new Object();
        grades['egoing'] = 10;
        grades['kk8805'] = 6;
        grades['sorialgi'] = 80;
        
        
        grades['egoing']     //10
        grades['ego'+'ing']  //10
        grades.egoing        //10
// egoing, kk8805, sorialgi 는 키(key) 라고부름
// 10 6 80 은  value라고 부
```



