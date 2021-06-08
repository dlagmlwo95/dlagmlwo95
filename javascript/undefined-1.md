# 조건문 if else

{% hint style="info" %}
if  
조건문은 if로 시작한다.  if \(boolean\) {}  
boolean 부분이 true면 실행 false면 실행 X 하고나서 괄호 바깥 실행
{% endhint %}

```javascript
if(ture){
   alert('result : true');
}
```

{% hint style="info" %}
else문  
만약에 if부분이 true면 if만 실행, if부분이 false면 else실행
{% endhint %}

```javascript
          if(false){
              alert(1);
          } else if(true){
              alert(2);
          } else if (true){
              alert(3);
          } else {
              alert(4);
          }                     // 2

          if(false){
              alert(1);
          } else if(false){
              alert(2);
          } else if(true){
              alert(3);
          } else {
              alert(4);
          }                    // 3
```



변수와 비교연산자

{% hint style="info" %}
&& 는 and  
\|\|  or
{% endhint %}

```javascript
          var id = prompt('아이디를 입력해주세요.');
          if (id == 'egoing'){
              var password = prompt('비밀번호를 입력해주세요')
              if(password == '111111'){
                  alert('로그인 하셨습니다.' + id +'님 반갑습니다.');
              } else {
                alert('비밀번호가 다릅니다.');
              }
          } else {
              alert('아이디가 일치하지 않습니다.');
          }

/*-------------------------------------------------------------*/
//정
          // && = and    || = or
          var id = prompt('아이디를 입력해주세요.');
          var password = prompt('비밀번호를 입력해주세요')
          if (id == 'egoing' && password == '111111'){
                  alert('로그인 하셨습니다.' + id +'님 반갑습니다.');
          } else {
              alert('아이디가 일치하지 않습니다.');
          }
```

```javascript
//&&와 ||를 이용한 예제

          var id = prompt('아이디를 입력해주세요');
          password = prompt('비밀번호를 입력해주세요');
          if((id === 'egoing' || id === 'agoign' || id === 'cgoing') && password ==='11111'){
          alert('인증했습니다.');    
          }else{
              alert('인증에 실패 했습니다.')
          }
```

