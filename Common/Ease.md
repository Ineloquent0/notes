参考：https://easings.net/

![ease](https://raw.githubusercontent.com/Ineloquent0/notes/main/images/ease.jpg)


名称        | 方法
---         | ---
InSine      | `1 - Math.cos((x * Math.PI) / 2)`
OutSine     | `Math.sin((x * Math.PI) / 2)`
InOutSine   | `-(Math.cos(Math.PI * x) - 1) / 2`
InQuad      | `x * x`
OutQuad     | `1 - (1 - x) * (1 - x)`
InOutQuad   | `x < 0.5? 2 * x * x : 1 - Math.pow(-2 * x + 2, 2) / 2`
InCubic     | `x * x * x`
OutCubic    | `1 - Math.pow(1 - x, 3)`
InOutCubic  | `x < 0.5? 4 * x * x * x : 1 - Math.pow(-2 * x + 2, 3) / 2`
InQuart     | `x * x * x * x`
OutQuart    | `1 - Math.pow(1 - x, 4)`
InOutQuart  | `x < 0.5? 8 * x * x * x * x : 1 - Math.pow(-2 * x + 2, 4) / 2`
InQuint     | `x * x * x * x * x`
OutQuint    | `1 - Math.pow(1 - x, 5)`
InOutQuint  | `x < 0.5? 16 * x * x * x * x * x : 1 - Math.pow(-2 * x + 2, 5) / 2`
InExpo      | `x === 0? 0 : Math.pow(2, 10 * x - 10)`
OutExpo     | `x === 1 ? 1 : 1 - Math.pow(2, -10 * x)`
InOutExpo   | `x === 0 ? 0 : x === 1 ? 1 : x < 0.5 ? Math.pow(2, 20 * x - 10) / 2 : (2 - Math.pow(2, -20 * x + 10)) / 2`
InCirc      | `1 - Math.sqrt(1 - Math.pow(x, 2))`
OutCirc     | `Math.sqrt(1 - Math.pow(x - 1, 2))`
InOutCirc   | `x < 0.5 ? (1 - Math.sqrt(1 - Math.pow(2 * x, 2))) / 2 : (Math.sqrt(1 - Math.pow(-2 * x + 2, 2)) + 1) / 2`
InElastic   | `x === 0 ? 0 : x === 1 ? 1 : -Math.pow(2, 10 * x - 10) * Math.sin((x * 10 - 10.75) * ((2 * Math.PI) / 3))`
OutElastic  | `x === 0 ? 0 : x === 1 ? 1 : Math.pow(2, -10 * x) * Math.sin((x * 10 - 0.75) * ((2 * Math.PI) / 3)) + 1`
InOutElastic| `x === 0 ? 0 : x === 1 ? 1 : x < 0.5 ? -(Math.pow(2, 20 * x - 10) * Math.sin((20 * x - 11.125) * ((2 * Math.PI) / 4.5))) / 2 : (Math.pow(2, -20 * x + 10) * Math.sin((20 * x - 11.125) * ((2 * Math.PI) / 4.5))) / 2 + 1`
InBack      | `c1 = 1.70158; c3 = c1 + 1; ` <br/> `c3 * x * x * x - c1 * x * x`
OutBack     | `c1 = 1.70158; c3 = c1 + 1; ` <br/> `1 + c3 * Math.pow(x - 1, 3) + c1 * Math.pow(x - 1, 2)`
InOutBack   | `c1 = 1.70158; c2 = c1 * 1.525; ` <br/> `x < 0.5 ? (Math.pow(2 * x, 2) * ((c2 + 1) * 2 * x - c2)) / 2 : (Math.pow(2 * x - 2, 2) * ((c2 + 1) * (x * 2 - 2) + c2) + 2) / 2`
InBounce    | `1 - OutBounce(1 - x)`
OutBounce   | `OutBounce(x)`
InOutBounce | `x < 0.5 ? (1 - OutBounce(1 - 2 * x)) / 2 : (1 + OutBounce(2 * x - 1)) / 2`



``` javascript
function OutBounce(x: number): number {
    const n1 = 7.5625;
    const d1 = 2.75;

    if (x < 1 / d1) {
        return n1 * x * x;
    } else if (x < 2 / d1) {
        return n1 * (x -= 1.5 / d1) * x + 0.75;
    } else if (x < 2.5 / d1) {
        return n1 * (x -= 2.25 / d1) * x + 0.9375;
    } else {
        return n1 * (x -= 2.625 / d1) * x + 0.984375;
    }
}
```






































