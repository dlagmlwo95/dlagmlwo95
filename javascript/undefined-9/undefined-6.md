# 배열

{% hint style="info" %}
배열 \[ \]
{% endhint %}

배열의 기

```javascript
1        var member = ["egoing" , "k8806" , "sorialgi"];
        alert(member[0]); // egoing
        
        
        
        
        
2        function get_members(){
            return ["egoing" , "k8806" , "sorialgi"];
        }
        var members = get_members();
        document.write(members[0]); // 이런식으로 출력 가능
```

배열과 반복문

```javascript
        function get_members(){
            return ["egoing" , "k8806" , "sorialgi"];
        }
        var members = get_members();
        // i < members.length 로 하면 멤버가 몇명이든 자동으로 같이 바뀌게됨. 
        for (var i = 0; i < members.length; i++){
            document.write([i].toUpperCase()+ "<br/>");//toUpperCase() 대문자
```

  


{% hint style="info" %}
배열 명령

```javascript
var li = ['a','b','c','d','f'];
li.push('f');   // push맨뒤에 하나 추가하기 명령어
li = li.concat(['f','g']);  //concat맨뒤에 여러개 추가하기 명령어
li.unshift('z');  //unshift 맨앞에 추가하기(원래있던건 하나씩 밀림)
li.splice(2,1,'e');    //splice 중간에 끼워넣기 (2) 3번째 있는걸 1개 삭제하고 e를 넣어라)
li.splice(3,2,'e');    //splice 4번째부터 2개를 삭제하고 e를 넣어라
li.shift();     //맨앞에 있는걸 삭제하라
li.pop();       //맨뒤에 있는걸 사제하라
li.sort();      //알파벳 숫자 순서로 정렬 sort(sortfunc)  <원하는 조작 정렬로 만들 수 있음.
li.reverse();   //알파 숫자 역순으로 정렬
```
{% endhint %}

