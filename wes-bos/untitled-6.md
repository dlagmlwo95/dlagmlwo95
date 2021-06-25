# Array

{% hint style="info" %}
## Array.prototype.map\(\)

map\(\) 메서드는 배열 내의 모든 요소 각각에 대하여 주어진 함수를 호출한 결과를 모아 새로운 배열을 반환합니다.
{% endhint %}

```javascript
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

{% hint style="info" %}
## Array.prototype.sort\(\) 

sort\(\) 메서드는 배열의 요소를 적절한 위치에 정렬한 후 그 배열을 반환합니다. 정렬은 stable sort가 아닐 수 있습니다. 기본 정렬 순서는 문자열의 유니코드 코드 포인트를 따릅니다.
{% endhint %}

```javascript
const months = ['March', 'Jan', 'Feb', 'Dec'];
months.sort();
console.log(months);
// expected output: Array ["Dec", "Feb", "Jan", "March"]

const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// expected output: Array [1, 100000, 21, 30, 4]
```

{% hint style="info" %}
## Array.prototype.reduce\(\)

reduce\(\) 메서드는 배열의 각 요소에 대해 주어진 리듀서\(reducer\) 함수를 실행하고, 하나의 결과값을 반환합니다.
{% endhint %}

```javascript
const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));
// expected output: 15

```



동영상코드

```markup
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
  </head>
  <body>
    <script>
      const inventors = [
        { first: "Albert", last: "Einstein", year: 1879, passed: 1955 },
        { first: "Isaac", last: "Newton", year: 1643, passed: 1727 },
        { first: "Galileo", last: "Galilei", year: 1564, passed: 1642 },
        { first: "Marie", last: "Curie", year: 1867, passed: 1934 },
        { first: "Johannes", last: "Kepler", year: 1571, passed: 1630 },
        { first: "Nicolaus", last: "Copernicus", year: 1473, passed: 1543 },
        { first: "Max", last: "Planck", year: 1858, passed: 1947 },
      ];

      const people = [
        "Bernhard, Sandra",
        "Bethea, Carl",
        "Beckett, Samuel",
        "Beddoes, Mick",
        "Beecher, Henry",
      ];

      //1. 1500년대에 태어난 사람들을 위해 발명가의 명단
      const fifteen = inventors.filter(
        (inventor) => inventor.year >= 1500 && inventor.year > 1600
      );
      console.table(fifteen);

      //array.prototype.map()
      // 2. 재고목록의 배열과 이름
      const fullNames = inventors.map(
        (inventor) => `${inventor.first} ${inventor.last}`
      );
      console.log(fullNames);

      //array.prototype.sort()
      //3.발명가를 첫째부터 막내까지 출생일로 분류하다.
      const ordered = inventors.sort((a, b) => (a.year > b.year ? 1 : -1));
      console.table(ordered);

      //array.prototype.reduce()
      //4. 모든 발명가들은 몇 년을 살았습니까?
      const totalYears = inventors.reduce((total, inventor) => {
        return total + (inventor.passed - inventor.year);
      }, 0);

      
      //5.발명가들은 생존 년수를 기준으로 분류한다.
      const oldest = inventors.sort(function (a, b) {
        const lastGuy = a.passed - a.year;
        const nextGuy = b.passed - b.year;
        return lastGuy > nextGuy ? -1 : 1;
      });
    </script>
  </body>
</html>

```



