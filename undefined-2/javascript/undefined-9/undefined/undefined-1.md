# 클로저

## 외부함수와 내부함

```javascript
//외부함
function outter(){
//내부함
    function inner(){
        var title = 'coding everybody'; 
        alert(title);
    }
    inner();
}
outter();


//외부함
function outter(){
//외부함수의 지역변
    var title = 'coding everybody';  
    //내부함
    function inner(){        
        alert(title);
    }
    inner();
}
outter();
```

## private variable

```javascript
function factory_movie(title){
    return {
        get_title : function (){
            return title;
        },
        set_title : function(_title){
            title = _title
        }
    }
}
ghost = factory_movie('Ghost in the shell');
matrix = factory_movie('Matrix');
 
alert(ghost.get_title());
alert(matrix.get_title());
 
ghost.set_title('공각기동대');
 
alert(ghost.get_title()); //공각기동대
alert(matrix.get_title());  // Matirx
```

```javascript
var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(id) {
        return function(){
            return id;
        }
    }(i);
}
for(var index in arr) {
    console.log(arr[index]());
} //  0 1 2 3 4
```

