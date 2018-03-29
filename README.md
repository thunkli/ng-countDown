# ng-countdown

## Installation
### HTML:
```html
<span id="countDown"></span>
```
## Usage
```js
import CountDown from 'ng-countdown/src/index.ts';
```

```js
new Countdown(document.getElementById("countDown"), {
    date: "June 7, 2087 15:03:25"
})
```
```js
new Countdown(document.getElementById("countDown"), {
    date: +(new Date) + 1000 * 60 * 60 * 24,
    render: function (data) {
      this.el.textContent = `${this.leadingZeros(data.hours, 2)}小时${this.leadingZeros(data.min, 2)}分${this.leadingZeros(data.sec, 2)}秒`
    }
})
```
```js
new Countdown(document.getElementById("countDown"), {
    date: +(new Date) + 10000,
    render: function (data) {
        this.el.textContent = this.leadingZeros(data.sec, 2) + " 秒"
    },
    onEnd: function () {
        console.log("ended")
    }
})
```
