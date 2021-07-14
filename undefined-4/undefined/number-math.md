# Number, Math

## toString\(\)

```javascript
//10진수 -> 2진수/16진수

let num = 10;
num.toString(); // "10" 숫자 -> 문자
num.toString(2); // "1010" 숫자를 2진수로 나타냄

let num2 = 255;
num2.toString(16); // "ff"
```

### Math.ceil\(\) : 올림

### Math.floor\(\) : 내림

### Math.round\(\) : 반올림

### toFixed\(\) : 소수점 자릿수\(문자\) 

```javascript
//문제: 소수점 둘째자리 까지 표현(셋째 자리에서 반올림)
let userRate = 30.1234;

// 1 답
Math.round(userRate * 100)/100  //30.12
// 2 답
Numbr(userRate.toFixed(2)); //30.12
```

### isNaN\(\) : NaN인지 판단

```javascript
let x = Number('x')// NaN

    x == NaN // false
    x === NaN // false
    NaN === NaN // false
    
    isNaN(x) // true
    isNaN(3) // false
```

### parseInt\(\) : 문자열을 숫자로 변

### parseFloat\(\) : 부동소수점을 반환한다.

### Math.random\(\) : 0 - 1사이 무작위 숫자 생성

```javascript
//문제: 1 - 100 사이의 숫자를 뽑고 싶다면?
Math.floor(MMath.random()*100)+1
```

### Math.max\(\) : 최대값

### Math.min\(\) : 최소값

### Math.abs\(\) : 절대값

### Math.pow\(n,m\) : 제곱값

### Math.sqrt\(\) : 제곱

