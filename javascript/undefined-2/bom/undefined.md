# 창 제어

## window open

* 새로운 윈도우를 오픈하는 역할을 하는 것이 윈도우오픈 메소드

```markup
<!--새 창에 열림 기본값-->
<input type="button" onclick="open1()" value="window.open('demo2.html');" />
<!-- 현재 창에 열림 '_self'-->
<input type="button" onclick="open2()" value="window.open('demo2.html', '_self');" />
<!-- 새 창에 열림 기본값 '_blank'-->
<input type="button" onclick="open3()" value="window.open('demo2.html', '_blank');" />
<!-- 새 창에 열리고 열려있으면 그곳에 열림 'ot'-->
<input type="button" onclick="open4()" value="window.open('demo2.html', 'ot');" />
<!-- 새 창의 크기도 함께 조절 resizable=yes -->
<input type="button" onclick="open5()" value="window.open('demo2.html', '_blank', 'width=200, height=200, resizable=yes');" />
```

### 팝업 차단

브라우저 업체들이 팝업을 기본적으로 차단하고 사용자가 팝업을 허용하는 경우에만 열리게 함. \(보안성\)

