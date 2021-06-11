# 문서의 기하학적 특성

```markup
<style>
    body{
        padding:0;
        margin:0;
    }
    #target{
        width:100px;
        height:100px;
        border:50px solid #1065e6;
        padding:50px;
        margin:50px;
    }
</style>
<div id="target">
    Coding
</div>
<script>
//위치를 알려줌.(거리) 결과 : 밑에 이미지처럼 뜸. 가로세로는 포함 X
var t = document.getElementById('target');
console.log(t.getBoundingClientRect());
</script>
```

![](../.gitbook/assets/image%20%288%29.png)

## 뷰포트 

setInterval \(\){}  
window.pageYOffset : 스크롤한정도  
getBoundingClientRect :뷰포트에서 엘리먼트까지의 정도

## 스크롤

```markup
<input type="button" id="scrollBtn" value="scroll(0, 1000)" />
<script>
    document.getElementById('scrollBtn').addEventListener('click', function(){
        window.scrollTo(0, 1000); // 0 은 x, 1000은 y
    })
</script>
```

## 스크린의 크기

```markup
<script>
//innerWidth : 뷰포트의 크기 innerHeight
console.log('window.innerWidth:', window.innerWidth, 'window.innerHeight:', window.innerHeight);
//screen .width 사용자모니터크
console.log('screen.width:', screen.width, 'screen.height:', screen.height);
</script>
```

