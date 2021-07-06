# 18. 클래스

```javascript
class Counter {
    constructor(runEveryFiveTime){
    this.counter = 0;
    this.callback = runEveryFiveTime;
    }

    increase(){
        this.counter++;
        console.log(this.counter);
        if(this. counter % 5 === 0){
            this.callback && this.callback(this.counter);
    }
}
//5
function printSomething(num) {
    console.log(`yo! ${num}`);
}

const coolCounter = new Counter();
coolCounter.increase();
coolCounter.increase();
coolCounter.increase();
```

