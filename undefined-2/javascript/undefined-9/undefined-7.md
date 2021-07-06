# 객체



{% hint style="info" %}
객체 { }  
배열은 순서가 있고, 객체는 순서가 없고 key와 value가 있음
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



//배열은 순서가 있고 객체는 순서가 없고 key와 value가 있음
        var arr = ['a','b','c'];
        for(var i = 0; i< arr.length;i++){
            console.log(arr[i]);
        }
```



```javascript
var grades = {'egoing' : 10, 'kk8805' : 6, 'sorialgi':80};
for(key in grades){
    console.log(key)
}  //egoing, kk8805, sorialgi
for(key in grades){
    console.log(grades[key])
}  //10, 6, 80

var grades = {'egoing' : 10, 'kk8805' : 6, 'sorialgi':80};
for(var key in grades){
    document.write("key: " + key + " value : " + grades[key] + "<br />");
}
```

```javascript
        var grades = {
            'list' : {'egoing' : 10, 'kk8805' : 6, 'sorialgi':80},
            'show' : function(){
                console.log(this.list); 
            }//this는 정해져 있는 변수  (여기서 이 함수를 가르키는(grades) 변수)
        } // 'egoing' : 10, 'kk8805' : 6, 'sorialgi':80
        grades['show']();     //grades.show(); 이거와 같음

        var grades = {
            'list' : {'egoing' : 10, 'kk8805' : 6, 'sorialgi':80},
            'show' : function(){
                for(var name in this.list){
                    console.log(name, this.list[name]);
                }
            }
        } 
        grades.show();  
        //객체지향프로그램 : 연관되어 있는 값과 연관되어 있는 처리를 그룹핑 해놓은것
```

