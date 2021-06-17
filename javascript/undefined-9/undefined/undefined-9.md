# 유효범위

```javascript
var vscope = 'global';
function fscope(){
    var vscope = 'local';
    alert(vscope);
}
fscope();  //local

//여기서 local은 지역변수, global은 전역변수
//지역변수는 그 지역(함수안)에서만 가능하다.
```

