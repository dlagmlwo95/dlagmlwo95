# 리팩토링\(refactoring\)

## 18화 리팩토링\(refactoring\)

  
리팩토링 : 코드를 깔끔하게\(효율적으로\) 만드는 것

```markup
    <input id="night_day" type="button" value="night" onclick="
    if(document.querySelector('#night_day').value === 'night'){
        document.querySelector('body').style.backgroundColor = 'black';
        document.querySelector('body').style.color = 'white';
        document.querySelector('#night_day').value = 'day'
    } else {
        document.querySelector('body').style.backgroundColor = 'white';
        document.querySelector('body').style.color = 'black';
        document.querySelector('#night_day').value = 'night';
     }
    ">
------------------------------------------------------------------------    
여기서 var을 이용하 중복되는 코드를 깔끔하게 만들어준다.
    <input type="button" value="night" onclick="
    var target = document.querySelector('body');
    if(this.value === 'night'){
        target.style.backgroundColor = 'black';
        target.style.color = 'white';
        this.value = 'day';
    } else {
        target.style.backgroundColor = 'white';
        target.style.color = 'black';
        this.value = 'night';
     }
    ">
```



